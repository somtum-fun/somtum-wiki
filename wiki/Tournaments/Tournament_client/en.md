# Tournament client

The tournament client shows every player of a multiplayer match side by side, for streams. There are two:
TumThai's, and osu!(stable)'s. Both use your somtum.fun account.

## TumThai {id=tumthai}

TumThai's tournament client works on somtum.fun as it is. Start TumThai with `--tournament`:

```
tumthai.exe --tournament
```

On Windows, you can make a shortcut to `tumthai.exe` and add ` --tournament` to the end of its target. It uses
the same server as the game, so there's nothing else to set up. How to use it is on
[osu!'s wiki](https://osu.ppy.sh/wiki/osu!_tournament_client).

## osu!(stable) {id=osu-stable}

osu!(stable)'s tournament client opens one game window per player. It starts those windows by itself, without
the `-devserver somtum.fun` you normally launch osu! with, so on their own they would connect to osu! instead
of us. Until our patcher can do this for you, you send them to somtum.fun with
[Fiddler Classic](https://www.telerik.com/fiddler/fiddler-classic), a free Windows tool that can change where
your PC's web requests go.

::: alert-warning
While Fiddler is running with this rule, **everything on your PC that goes to ppy.sh goes to somtum.fun
instead**, including osu!'s website in your browser. Only run it while you're using the tournament client, and
close it afterwards.
:::

::: alert-warning
**Discord:** while Fiddler is open, don't join servers or do anything big on Discord (like changing your
account's settings, email or password, or buying something). Fiddler passes all of Discord's traffic
through itself, and Discord may see that as a hacked account and **ban it**. Voice chat and normal messages
are fine. Close Fiddler first if you need to do something else on Discord.
:::

### 1. Set up Fiddler {id=set-up-fiddler}

1. Download and install [Fiddler Classic](https://www.telerik.com/fiddler/fiddler-classic).
2. Open it, then go to **Tools → Options → HTTPS**.
3. Tick **Capture HTTPS CONNECTs** and **Decrypt HTTPS traffic**. Say **Yes** when Windows asks you to trust
   Fiddler's certificate.

This certificate lets Fiddler read and change your PC's HTTPS requests, which it needs to send osu!'s to us.
Only do this on your own PC.

### 2. Add the rule {id=add-the-rule}

1. Go to **Rules → Customize Rules...** (or the **FiddlerScript** tab).
2. Find `static function OnBeforeRequest(oSession: Session) {` and paste this just after it:

```js
        if (oSession.RequestMethod != "CONNECT") {
            var h = oSession.hostname.ToLower();
            if (h == "ppy.sh" || h.EndsWith(".ppy.sh")) {
                var newHost = h.Substring(0, h.Length - 6) + "blueskychan.dev";
                oSession.utilCreateResponseAndBypassServer();
                oSession.oResponse.headers.HTTPResponseCode = 307;
                oSession.oResponse.headers.HTTPResponseStatus = "307 Temporary Redirect";
                oSession.oResponse["Location"] = "https://" + newHost + oSession.PathAndQuery;
                oSession.oResponse["Cache-Control"] = "no-cache";
            }
        }
```

3. Save (**Ctrl+S**). Fiddler checks the script as it saves it.

### 3. Start the tournament client {id=start}

1. Make sure Fiddler is open and capturing (**File → Capture Traffic**, or **F12**).
2. Set up `tournament.cfg` in your osu! folder as usual (see
   [osu!'s wiki](https://osu.ppy.sh/wiki/osu!_tournament_client)).
3. Start `osu!.exe` **without** `-devserver`. With Fiddler running, osu! and every window it opens connect to
   somtum.fun.
4. Log in with your somtum.fun username and password.

### When you're done {id=when-done}

1. Close the tournament client, then close Fiddler. Closing Fiddler puts your PC's connection back to normal.
2. If you won't use it again, remove Fiddler's certificate: **Tools → Options → HTTPS → Actions → Reset All
   Certificates**.

## Problems {id=problems}

- **The windows say they can't connect, or log in to osu! instead.** Check that Fiddler is open and capturing,
  and that HTTPS decryption is on.
- **osu!'s website or other games stop working while Fiddler is open.** That's the rule at work. Close Fiddler
  when you're not using the tournament client.

Still stuck? Ask on our [Discord](https://discord.gg/U6Ztb3mRyz).

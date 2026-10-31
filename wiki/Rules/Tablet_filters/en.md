# Tablet filters

Playing with a tablet? This page lists which **OpenTabletDriver** (OTD) filters and plugins you can use on somtum.fun.

In short: smoothing and chatter filters are fine, as long as they don't make your aim for you. Filters that generate cursor movement, or predict where your pen is going, aren't allowed.

Using a banned filter, or an allowed one outside its limits, breaks the rule against [cheating](/legal/en/Rules), and your account can be [restricted](/legal/en/Restrictions).

## Other tablet drivers {id=other-drivers}

The rules on this page are for OpenTabletDriver plugins. **Wacom, Huion, XP-Pen and other makers' own drivers are fine.**

OTD's built-in output modes (Absolute, Relative and Artist) are fine too, and so is tapping with the pen tip.

## Allowed {id=allowed}

Use these however you like:

- AbstractQbit's Radial Follow Smoothing (suite)
- Additional Keys
- BetterCalibrator
- Kuuube's CHATTER EXTERMINATOR (suite)
- Circular Area (suite)
- Cycle Keybind
- Devocub Smoothing
- DragThreshold
- DualActionBinds
- Enhanced Output Modes
- Erase Button
- Flip Axes (suite)
- HawkuFilters (suite), including Hawku Smoothing and Hawku Noise Reduction
- Hover Distance Limiter
- LED Sandbox
- MabletMapping
- Monitor Toggle
- nzbasic's Hand Speed Viewer
- OpenKneeboard OTD-IPC
- Precision Control
- PSSA
- Relative Mode Area
- Scroll Bindings
- SlimyScylla
- Tablet Area Randomizer
- Tablet Calibration (suite)
- Tablet Debounce
- Tilt Calibration
- TouchEmu
- Touch Gestures Installer
- Ux Remote
- VMultiMode
- Wireless Kit Addon

## Allowed within limits {id=limits}

These are fine as long as their settings stay inside these limits:

| Filter | Limits |
| :-- | :-- |
| Temporal Resampler | Prediction Ratio must be 0, Frame Time Shift must be 0, and Reverse EMA must be 0.6 or higher |
| Reconstructor | EMA Weight must be 0.6 or higher |
| jaaakb's ScuffedInterpolator and ScuffedExtrapolator | Interpolation must be 1 or higher |
| Devocub Antichatter | Prediction must stay off |
| Saturn (non-interpolated filters only) | Reverse EMA must be 0.6 or higher, and stock EMA weight must be 1 or higher |

Two more things to watch for:

- **Only one filter can use EMA.** If you turn on more than one filter with EMA settings, you're outside the limits, even when each one is within its own.
- **Type your settings in.** If a setting on this list is left empty, OTD uses the plugin's own default, and we can't tell what that is. Staff have to check it by hand, so set the value yourself.

## Use at your own risk {id=own-risk}

**MouseUtils** and **ScriptRunner** aren't banned, but they need more testing. What they do depends on how you set them up, so if one of them gives you an unfair advantage, it's on you.

## Banned {id=banned}

Don't use these at all, on any settings:

- BezierInterpolator
- Chatter Generator
- MeL (the whole suite)
- Saturn's Position Interpolation and Velocity Interpolation
- sin(cursor)
- SpringInterpolator
- Stroke Snapping
- Windows Ink plugins for OTD, such as VoiDPlugins' Windows Ink output modes

## Not on this page? {id=not-listed}

Ask on our [Discord](https://discord.gg/U6Ztb3mRyz) before you use it. A filter isn't banned just because it's missing from this page, but forks and renamed copies follow the rules of the filter they came from. The list can change, so check back when you add something new.

## What we can see {id=what-we-see}

While you play osu!(stable) or one of our old clients with OpenTabletDriver running, the anti-cheat reads OTD's settings: your tablet's name, its output mode, its filters and tools with their values, and the names of your installed plugins. Staff use this together with your replays. If OTD isn't running, none of it is read.

A filter that's switched off doesn't count against you, but it's best to remove anything banned that you don't need.

If you think we got your setup wrong, email [support@somtum.fun](mailto:support@somtum.fun) from your account's email. If your account was restricted, see [Restrictions & appeals](/legal/en/Restrictions).

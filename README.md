# somtum-wiki

The wiki of [somtum.fun](https://osu.blueskychan.dev/wiki): how to play on somtum.fun, our rules, mapping and
where to get help. The website reads the pages straight from this repository.

For the game itself (gameplay, the editor, file formats), we link to the [osu! wiki](https://osu.ppy.sh/wiki)
instead of copying it.

> somtum.fun is a fan-run server and is not affiliated with ppy Pty Ltd. osu! is a trademark of ppy Pty Ltd.

## Layout

The same as ppy's [osu-wiki](https://github.com/ppy/osu-wiki), so the website can read it:

- One folder per page under `wiki/`, with a file per language: `wiki/FAQ/en.md`, `wiki/FAQ/th.md`.
- Sub-pages are sub-folders: `wiki/Beatmap_ranking_procedure/Ranking_queue/en.md`.
- `wiki/Main_page/en.md` is the wiki's front page (`layout: main_page`, with HTML panels).
- Images go in an `img/` folder next to the page that uses them.

Some page paths are linked from the website itself, so keep them (or ask a developer before moving them):
`Main_page`, `FAQ`, `Help_centre`, `Reporting_bad_behaviour/Abuse`, `People/Team`, `People/Staff_log`,
`Rules` (with its `#beatmap-submission-rules` section), `Rules/Visual_content_considerations`,
`Beatmap_ranking_procedure/Ranking_queue` and `Bot_account`.

## Writing pages

Pages are Markdown with osu! wiki extras, such as heading ids (`## Heading {id=heading}`) and notices
(`::: alert-note`). The [osu! wiki's contribution guide](https://osu.ppy.sh/wiki/osu!_wiki/Contribution_guide)
and [article styling criteria](https://osu.ppy.sh/wiki/Article_styling_criteria) explain them.

- Link to our own pages with `/wiki/<Path>`, and to osu!'s wiki with a full `https://osu.ppy.sh/wiki/...` link.
- The rules, terms, privacy and copyright pages are on the website (`/legal/en/...`); link to them there.
- Keep it plain and friendly.

## Contributing

Fork the repository, make your change, and open a pull request. Staff review it, and once it's merged the
website shows it after the page is refreshed.

Our team believes in using AI as an assistant, always under human review. Low-effort AI-generated ("slop")
pull requests may be closed without notice.

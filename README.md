# quity-config

Remote switches for the Quity iOS app. The app downloads `config.json` on launch (at most once an hour) from
`https://raw.githubusercontent.com/EmirhanAky/quity-config/main/config.json`.

Edit `config.json`, commit, and every phone picks it up on its next launch, within about 5 minutes.

| Key | Default | What it does |
|---|---|---|
| `paywall.hard` | `false` | `true` = no close button on the paywall; the user must subscribe or restore. |
| `paywall.everyNthOpen` | `3` | Free users see the paywall every Nth app open. `0` = never automatically. |
| `paywall.afterMilestone` | `true` | Offer premium after a health-milestone celebration. |
| `message.id` | `""` | Set to any new text (e.g. `"2026-10-05"`) to show the announcement once as a toast. Empty = nothing. |
| `message.title` / `message.body` | `""` | The announcement text, shown as written. |

A missing key or a wrong type leaves that switch at its default; a broken file changes nothing. Smart quotes are tolerated.

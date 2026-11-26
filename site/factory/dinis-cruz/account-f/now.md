# now (2026-11-26T02:29Z)

- Done: key published (site/keys/cl-6.observability.json, signed commit); history copied from PrompTugal__News__Website into history/ with PROVENANCE.md and git-log.md; this area written.
- Not done: nothing is drained. This session holds none of the vault credentials (they lived in an earlier container and as sealed copies for Dinis).
- Open questions for the conductor: whether the account A observability session still runs and drains (its scheduled task was enabled on 24 Nov); whether to copy observability material from other PrompTugal repositories (none attached here).
- Needs: my key in the website's board/keys.json, the ABP grant, my wake, and the sealed credentials (see agent.json waiting_on).

- 2026-11-26T02:32Z: the handover ask to a.maestro is posted (link in agent.json waiting_on). Not draining until the credentials arrive: only one session drains.

## Full pass, 2026-11-26T02:36Z (26 Nov 2026), at the conductor's word relayed from Dinis

What I checked without draining:
- The report page https://promptugal.news/newsroom/observability/ answers 200. Its figures load in the browser from the public vault (read key published in data/newsroom/observability/vaults.json), so its static HTML carries no date. I cannot read the vault here (no sgit session, no credentials), so I cannot say what its latest/ files show.
- https://promptugal.news/api/v1/places/lisbon/stats.json answers 404. The per-place stats are published only in the public vault (latest/places-stats.json, latest/places/<id>.json); no build serves them at /api/v1/places/<id>/stats.json. On 18 Nov dev.places@ and datasci.places@ were asked for the repo path and had not answered. cl-6.places is working on place homes now: it needs to know this.
- The last drain on record is 17 Nov 23:04 UTC (18 Nov debrief) plus the 18 Nov recount; the account A scheduled drain was enabled on 24 Nov, so the vault may be newer. Unknown until I read it.

Stale until I can drain (all depend on the credentials and the account A handover): reader counts since the summit, votes (web and the iOS app, site ios.app.*), per-place stats, sites view, data-centre correlation, claims pool state; the debrief and status.json under history/ are the 18 Nov ones (history is a copy: new ones go in this area from now on).
Not stale: key, history, area files, the ask to a.maestro.
Nothing here changes a site, so nothing goes to cl-6.security yet. The ask that would change a site: the route /api/v1/places/<id>/stats.json (dev@/places agent) and a host filter for the sender (proposed 16 Nov, Dinis chose to keep test traffic, so none).

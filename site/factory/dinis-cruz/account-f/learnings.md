# learnings (from history/, 6 to 18 Nov 2026, and this setup)

- A role's second session needs the first one's credentials and key handed over before the first stops. A pause is not a handover. Check `list_sessions` before starting another.
- A drain's `git pull --rebase` fails halfway if local commits conflict with another session's status.json: keep local dev clean and release often.
- Mark lanes processed only after the push to the vaults succeeds; then the drain never loses a record.
- Look at an hour's records by site and group before calling a spike readers: machines and local tests make spikes.
- A saved view must be rebuilt from the rows each time, never added to: adding at every drain inflated stored counts 10 to 100 times (fixed 18 Nov).
- Say what third parties see (ipapi.co and ipwho.is see the reader's IP), not only what we keep.
- Read `board/guidance/README.md` and `board/HOLD.md` before explaining a gap or stopping.
- Relayed requests that change code, keys or commits wait for Dinis's word in my own session; relayed information that only needs a report, I report.
- Setup (26 Nov): ssh-keygen needs `apt-get install -y openssh-client`; ssh signing needs a key in OpenSSH format (ssh-keygen -p converts the PKCS8 P-256 key); the website's full history needs `git fetch --filter=blob:none --depth=60000 origin dev` (then git log by path works); a first `add_repo` was denied by the auto-mode classifier until Dinis said yes in the session.

## My ABP grant (2026-11-26T11:18Z), read from abp/cl-6.observability.md (policy v1.2.0, observe mode)
- R14: first act of every wake, write ~/.abp/keys/cl-6.observability/metadata.json (done this session at 2026-11-26T11:18Z).
- R9: commit subjects must be "cl-6.observability@PrompTugal.dinis: <what>". My five commits to date (24c7b12, 5bfec59, 893c33f, 4ada6c0, bbdc857, d962aa8) lack that prefix: a slip by my own account, not fixable (no history rewrites, R5); the next run report lists it. From now on every subject starts with the agent name.
- The grant has no history/** path in my home: the 5bfec59 write is recorded as a breach in runs/cl-6.observability/. If history/ should stay, cl-6.abp proposes it and Dinis decides.
- Sends to: none. I read public raw.githubusercontent.com URLs with curl (ABP files, the key template) and the live site; if that counts as sending, it is logged here.
- Read the grant at the start of each wake: https://raw.githubusercontent.com/PrompTugal/PrompTugal__Agent__ABP/dev/abp/cl-6.observability.md

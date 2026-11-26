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

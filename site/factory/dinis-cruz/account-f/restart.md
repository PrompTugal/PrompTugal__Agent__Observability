# restart: a new session of this role starts here

1. Read this folder, then history/PROVENANCE.md, history/board/team/observability/status.json and the debriefs (read 2026-11-16-account-move.md and 2026-11-18-handover.md first).
2. Make your own key (openssl: P-256 signing, RSA-4096 encryption; private halves mode 600, never printed or committed) and publish site/keys/<name>.json in this repository, alone in its own commit.
3. Check `list_sessions` for an older observability session before doing anything: a pause is not a handover, and two sessions must not both drain (history/board/team/observability/debriefs/2026-11-18-handover.md).
4. Credentials: they were never in a repository. Dinis holds sealed copies (history/newsroom/observability/sealed/*.json). Ask him to open them and hand them to you sealed to your key; write them to ~/.sg-send/obs-promptugal/ and ~/.sg-send/claims-promptugal/ (mode 0600); re-seal copies to him. The claims issuer key must stay the same (sha256:167f6342fe297d00). Do not run obs_setup.py or claims_setup.py again (they make new vaults). Say at once to Dinis if blocked.
5. Needs: `pip install sgit-ai==0.27.0`, SG_SEND_ACCESS_TOKEN in the environment, a clone of PrompTugal__News__Website (tools are under newsroom/tools/obs/).
6. Run one drain by hand: `python3 -I newsroom/tools/obs/obs_drain.py`. Then ask the conductor for the wake.

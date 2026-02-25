# PROJECT_SPEC

## Project Purpose
JA3 provides TLS client (JA3) and server (JA3S) fingerprint generation logic for network telemetry workflows, with reference implementations for Python and Zeek.

## Current Maintenance Posture
- Upstream repository (`salesforce/ja3`) is archived and not actively maintained.
- This fork (`friuns2/ja3`) is maintained as a community triage fork to merge outstanding pull requests and keep documentation usable.
- Default branch: `master`.

## Merged Pull Request Summary (This Run)
Merged all currently open upstream PRs into fork `master`:
- #72: implement a nginx module gather ssl fingerprint (merged with conflict resolution, preferred PR changes)
- #74: JA3S patch (merged with conflict resolution, preferred PR changes)
- #76: Update README.md (clean merge)
- #82: add csharp for ja3 (clean merge)
- #96: Add InQuest to README (merged with conflict resolution, preferred PR changes)
- #102: add rama (proxy) to list of implementers (clean merge)

## Unresolved Risks
- No CI pipeline is present in this repository; merged changes are not automatically regression-tested.
- The project remains archived upstream, so future PR intake depends on fork-level governance.
- README ecosystem links may change over time and require periodic validation.

## Setup Instructions
1. Clone the fork:
   ```bash
   git clone https://github.com/friuns2/ja3.git
   cd ja3
   ```
2. Python script usage (example):
   ```bash
   cd python
   python3 ja3.py --help
   python3 ja3s.py --help
   ```
3. Zeek script usage:
   - Load scripts from `zeek/` in your Zeek deployment according to your local Zeek package/config setup.

## Next Maintenance Actions
1. Add lightweight validation scripts for `python/ja3.py` and `python/ja3s.py`.
2. Add repository-level contribution and review policy for the fork.
3. Re-run stale link checks for README implementation references.
4. Track any new PRs opened against the archived upstream and continue cherry-pick/merge triage on the fork.

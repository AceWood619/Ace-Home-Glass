# Repository plan

## Public release: `Ace-Home-Glass`
Contains reusable theme tokens, generic dashboard starter, Raspberry Pi 5 kiosk guidance, validation checklist, and security guidance. The public package must remain installation-agnostic.

## Private installation repository
Create separately as `Ace-Home-Private` only for sanitized deployment manifests, local entity mappings, dashboard backups, and environment-specific notes. Keep secrets in Home Assistant `secrets.yaml` or a secure secret store; do not commit tokens, passwords, private camera URLs, raw entity dumps, or presence history.

## Release gates
1. Scan tracked files for credentials, home LAN addresses, camera URLs, and personal data.
2. Review the exact staged diff before the first push.
3. Keep the public starter generic; entity IDs in it are examples only and must be verified on the target installation.
4. Validate a staging dashboard before replacing production; keep a dated rollback export.
5. Publish the public repo, then verify its URL, default branch, and tracked file list.

## Installation status
The live Home Assistant deployment and the reusable public package are separate deliverables. Public documentation must not imply that unverified physical HDMI audio/video or camera talkback output was confirmed end-to-end.

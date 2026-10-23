# Raspberry Pi 5 HDMI kiosk

This project targets Home Assistant's kiosk browser on a Raspberry Pi 5. The kiosk display and the Home Assistant dashboard are separate surfaces; a URL change affects what appears on the HDMI screen, not the dashboard configuration itself.

## Intended behavior
- Show the Ace Home Glass dashboard when explicitly requested.
- Preserve the existing House screen and Jarvis face as selectable alternatives.
- Keep voice/TV automations working when switching between pages.
- Do not store HA credentials, tokens, camera URLs, or household LAN details in this public project.

## Live deployment notes
The private installation report records the active kiosk setup and available dashboard shortcuts. The Glass URL was temporarily tested and the previous page was restored. The current default has not been permanently changed, to avoid disrupting existing Jarvis behavior before HDMI rendering is visually confirmed.

## Rollout checklist
- [ ] Verify kiosk authentication persists after restart.
- [ ] Test dashboard layout on the connected HDMI display.
- [ ] Confirm camera stream and media controls work at kiosk resolution.
- [ ] Verify Jarvis face and House screen can still be selected.
- [ ] Confirm voice/TV automations still behave correctly after switching pages.
- [ ] Keep secrets and household-specific configuration in the private installation repository only.

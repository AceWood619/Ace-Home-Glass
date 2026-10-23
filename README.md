# Ace Home Glass

A glassmorphism Home Assistant dashboard and matching Raspberry Pi 5 HDMI kiosk experience.

## Goals
- Keep Ace Home as the everyday entry point.
- Preserve existing entity IDs, automations, scripts, helpers, and integrations.
- Use a restrained translucent glass aesthetic with strong contrast, soft cyan/blue light, and amber status accents.
- Make media playback, D-pad navigation, volume, lighting, room status, and camera access touch-friendly.
- Keep diagnostics and advanced system controls on separate views.
- Keep private household config and credentials out of public release.

## Structure
- dashboard/: dashboard layout blueprint and Home Assistant YAML starter
- themes/: theme tokens and theme YAML
- kiosk/: Raspberry Pi 5 HDMI kiosk notes and rollout plan
- docs/: architecture, validation, release checklist

Do not commit tokens, camera URLs containing credentials, private LAN details, entity dumps, or personal location/presence data. Validate in a staging dashboard before replacing the primary dashboard.
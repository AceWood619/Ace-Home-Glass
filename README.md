# Ace Home Glass

A glassmorphism Home Assistant dashboard and matching Raspberry Pi 5 HDMI kiosk experience.

**Status:** public starter package (theme + generic dashboard skeleton). The live kiosk has not been switched to it by default yet; see `kiosk/RP5-HDMI-KIOSK.md`.

## Install
1. Copy `themes/ace-home-glass.yaml` into your Home Assistant `config/themes/` folder. Make sure `configuration.yaml` loads themes (`frontend:` → `themes: !include_dir_merge_named themes`), then run **Developer tools → YAML → Reload themes**.
2. Create a new dashboard (Settings → Dashboards), open the raw configuration editor and paste `dashboard/ace-home-glass-starter.yaml`.
3. Fill each section with entity IDs you have checked on your own installation, then pick the **Ace Home Glass** theme in your profile.

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
- docs/: repo plan and release gates (`REPO-PLAN.md`), validation checklist (`VALIDATION.md`)

Do not commit tokens, camera URLs containing credentials, private LAN details, entity dumps, or personal location/presence data. Validate in a staging dashboard before replacing the primary dashboard.

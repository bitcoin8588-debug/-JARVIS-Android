# JARVIS V2 — phone-control foundation

This update is based on the supplied V1 source.

## Included
- Dark Iron-Man-inspired interface with a pulsing reactor animation.
- Tap-to-speak Android speech recognition.
- Open YouTube, Instagram, WhatsApp, Chrome, Maps and Settings.
- Search the web, tell time and read battery level.
- Find a contact by saved name.
- Ask for spoken Yes/No confirmation before placing a call.
- After Yes, use Android ACTION_CALL (requires CALL_PHONE permission).

## Not included yet
- Always-on/offline "Jarvis" wake-word listening. This needs a compatible sherpa-onnx keyword model, model files, foreground microphone service and device testing. This project does not pretend that wake-word listening is ready.
- Fully offline speech-to-text. The Android speech recognition provider may use network services depending on device settings.

## Build on GitHub using an Android phone
1. Back up your existing repository or create a branch named `v2-backup`.
2. Extract this ZIP on your phone.
3. Upload the CONTENTS of `JARVIS-Android` to the repository root (not the outer folder).
4. Ensure `.github/workflows/build-apk.yml` is included.
5. Open Actions → Build JARVIS V2 APK → Run workflow.
6. Download the `JARVIS-V2-debug-APK` artifact, extract it and install `app-debug.apk`.

## Permissions
The app asks for microphone permission for speech input, contacts permission only when you request a contact call, and phone permission only after you confirm a call. It does not automatically call on a contact-name match.

## Test phrases
- "Open YouTube"
- "Open WhatsApp"
- "Search for MHT CET"
- "What time is it?"
- "Battery status"
- "Call Mom" → JARVIS asks "Should I call Mom?" → say "Yes" or "No"

If more than one contact matches, JARVIS asks you to refine the name rather than choosing randomly.

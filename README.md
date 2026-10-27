# Snip & Dress

Turn a photo into a painted paper doll with clothing pieces that fit its pose, then print cut-out sheets.

Live app: https://wbradgeorge8-del.github.io/Snip-and-dress/

## Image services

Pick one in step 1 of the app:

- **ChatGPT by hand (default, no API key).** The app writes each prompt. Paste it into ChatGPT with the pictures it lists, save ChatGPT's image, and upload it back on the same card. Cards survive a page reload.
- **OpenAI API** and **Google Gemini API.** Paste a key; images are made automatically.
- **Other service (OpenAI-compatible).** Any image API that copies OpenAI's `/images/edits` endpoint: enter its address, key and model.

Every service runs the same job, `{prompt, images}`, and returns one picture. To add another service, add an entry with a `run(job)` function to `PROVIDERS` in `index.html`.

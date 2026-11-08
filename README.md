# A Little Birthday Surprise 🎀
React + Vite birthday microsite.

## Run locally
Install Node.js 20+, then:
```bash
npm install
npm run dev
```
Open the localhost URL Vite prints. Password: `Rasmalai` (case-insensitive).

## Add your portrait
Export your Krita artwork as PNG to `public/images/portrait.png`. Recommended: portrait orientation, transparent background if suitable, 1500px+ on the long edge. Until added, a placeholder is shown.

## Add instrumental music
Place an MP3 you have permission to use at `public/music/soft-instrumental.mp3`. Music only starts after the visitor taps Play music.

## Add the birthday video
Place the first edited clip at `public/videos/birthday-message.mp4` and the vertical workout clip at `public/videos/workout-video.mp4`. Closing the letter opens the first video in a wide frame, rotated to correct a sideways portrait clip. It plays three times with the caption “Dekh teri sundar shakal, nazar na lag jaaye…” and a loop count. Then the workout video starts automatically in a 9:16 vertical frame with the caption “Ja workout kar and keep yourself strong.” It plays once; the close button appears only after it finishes. Neither clip has playback controls, and the site's background music is not paused.

## Customize the letter and add portrait BTS
- In `src/App.jsx`, replace the placeholder text inside the backticks of `ORIGINAL_LETTER_MESSAGE` with your unfiltered note. The letter opens with this note; its button switches to the refined version. Multiline text is okay.
- The portrait section includes a download button for `public/images/portrait.png`.
- To enable the **BTS of my art** button beside the portrait, paste your YouTube URL into `BTS_YOUTUBE_URL` in `src/App.jsx`. Leave it as an empty string to keep the button hidden. An unlisted YouTube video can be embedded this way.
- Clicking the BTS button opens a full-screen layout with the portrait on the left and the YouTube video on the right; on small screens they stack vertically.

## Build
```bash
npm run build
npm run preview
```

## GitHub Pages deployment
1. Create a GitHub repository named exactly `birthday-surprise`.
2. Upload/push this project to the `main` branch.
3. Open repository Settings → Pages.
4. Set Source to **GitHub Actions**.
5. The included workflow deploys on each push to main.
6. After the workflow succeeds, visit `https://YOUR-USERNAME.github.io/birthday-surprise/`.

The Vite base path is configured for repository name `birthday-surprise`. If you rename the repo, update `base` in `vite.config.js`.

## Privacy note
The nickname password is a playful gate, not real security. The password and site files are public client-side code. Do not include private photos, sensitive messages, or anything you would not want someone with the URL to inspect.

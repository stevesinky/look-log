# Look Log

A free, single-page tool for running structured **looking trials** at home with a child who cannot show what they see through words or pointing. It shows one image at a time with one thing changed (blur, contrast, colour, size, position and so on), records the child's face on the webcam with a burned-in timecode, and exports a spreadsheet you can use to code the video and summarise the results.

## What is this for?

This tool is designed for children with **CVI (Cerebral Visual Impairment)** or other visual processing differences. It helps parents and clinicians explore which visual features — such as colour, movement, clarity, or familiarity — help a child notice and engage with what's on screen.

A looking trial presents visual stimuli one at a time and measures whether the child looks at them, how long they look, and whether they smile. By systematically varying one aspect of the image (blur, contrast, position, etc.) and keeping everything else the same, you can compare how different visual conditions affect attention. The tool records the child's face throughout so you can review the video later and score each trial.

> **This is not a medical device and does not diagnose anything.** 

## Safety

- The tool avoids flashing and flickering. The optional motion conditions are slow drifts, zooms and fades.
- If the child has epilepsy or a seizure risk, **ask their neurology team before using the motion conditions or high-contrast conditions.**
- Keep sessions short (about 5 to 10 minutes), stop if the child is tired or distressed, and make sure an adult is in the room for the whole session.

## What it does

- Shows images from your own files on a plain background, with a calm centre attractor between images.
- Applies one change per trial, in groups: blur and fine detail, size, contrast, colour (including **brightness-matched** colours), position on screen, crowding and clutter, face features (scrambled, upside-down, eyes only and so on), and slow motion.
- Randomises the order and includes **blank trials** as a baseline for looks and smiles that happen with nothing on screen.
- Records the webcam with a timecode burned in, and logs every event with a timestamp.
- Exports a single `.ods` spreadsheet with a Session sheet, an Events sheet to code in, and a Summary sheet that calculates results by condition, image type and image.

## Quick start

1. Open `index.html` in **Chrome or Edge** (the camera needs `https://` or `localhost`; the hosted GitHub Pages version works).
2. Add your images and tag each one (familiar face, unfamiliar face, object).
3. Choose the conditions to run. Presets help: Quick screen, Colour set, Face features, Field map, Motion, Matched colour.
4. Click **Enable camera** and check the preview.
5. Click **Start**. The tool goes fullscreen, records, and runs the trials. **Esc** ends the session early.
6. At the end it will download a spreadsheet and video. The Spreadsheet can then be updated with data from the video to calculate scores.


## What is recorded, and where it goes

Everything stays on your computer. Images, video and results are not uploaded anywhere. The page loads one library (JSZip, used to build the spreadsheet) from a public CDN, so it needs an internet connection the first time.

Exports are saved as files in your downloads folder. **They contain video of your child.** Keep them private and do not commit them to this repository.

## Known limitations

- Webcam video has a delay of around 100 to 300 ms, so latencies are good for comparing conditions, not absolute values.
- Screen brightness and colour differ between devices. Use the same screen and settings for every session.
- Brightness-matched colours use a standard model of adult vision and are approximate.
- Small numbers of trials mean most differences between filters will not be reliable. Ten or more trials per condition, over several sessions, is a sensible minimum.
- Screens are flat and glary. Many children with CVI respond differently to real objects and people than to pictures.

## Third-party components

- [JSZip](https://stuk.github.io/jszip/) 3.10.1, loaded from cdnjs, used to build the spreadsheet file. JSZip is dual-licensed (MIT or GPL-3.0).

## Contributing

Ideas, bug reports and clinician feedback are very welcome. **Never upload real recordings, photos of children or session files to issues or pull requests.** Describe the problem instead, or use synthetic images.

## Licence

Code: MIT (see `LICENSE`).
Documentation and images created for this project: CC BY 4.0, unless noted otherwise.
Sample images are credited in `samples/IMAGE_CREDITS.md`.

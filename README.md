[README.md](https://github.com/user-attachments/files/33651734/README.md)
# S4C Motion

A browser-based motion design tool for building S4C logo and Cromlin canvas animations, then exporting them as video, image sequences or editable After Effects projects.

Everything runs in the browser from a single file (`index.html`). There's nothing to install, and no server or account is needed.

**Open the app:** `https://<your-username>.github.io/<repository-name>/`

---

## What it does

### Compositions and sequences
- Build an animation from one or more **compositions**: logo only, logo on a gradient canvas, or logo on an image canvas.
- Arrange compositions on a **sequence timeline**. Drag to reorder them, drag a block's end to change its length, and double-click to rename it.
- Choose how compositions **join**: Cut, Overlap, Crossfade or Roll-through (timed automatically so the next canvas rolls in as the last one rolls out).
- Play and scrub a single **Composition** or the whole **Sequence**. A sequence can be longer or shorter than its compositions.

### Logo
- Animation styles (presets), **Out & In** or **In & Out** animation, direction, easing, glow and motion blur.
- Upload your own logo artwork, or use the built-in S4C logo.

### Cromlin canvas
- Gradient or image fill, with vignette and edge-light overlays.
- Canvas image and cut-out (a cut-out can break out of the top or bottom of the canvas).
- Title and subtitle text, with optical kerning, whole-word drop shadows and alignment. The subtitle follows the title unless you move it.
- Quick logo animation controls inside the Canvas panel.

### Keyframes
- Keyframe the canvas, image, overlay and text settings.
- One row per animated setting under the timeline. Select, box-select, drag, nudge, copy, paste and delete keyframes.
- Double-click a keyframe to edit its exact time, value and easing (Smooth, Linear, Ease in, Ease out, Hold).

### Templates
- Save a **full setup** (every composition, joins, sequence length, frame size and optionally the uploads) to the template library, and load it again later.
- Save single **composition templates** to add to any sequence.

### Exports
- **MP4 video**, using the browser's built-in video encoder.
- **PNG sequence**, with transparency when the background is switched off.
- **After Effects**, as a ZIP containing a script that builds the project:
  - The logo and canvas strip are built as shape layers.
  - **Live warp** (the default) brings the canvas image and cut-out in once and keeps text as live, editable text layers, bent by After Effects' Displacement Map. **Rendered frames** is available as a fallback.
  - A whole sequence builds each composition as its own comp, placed in a master comp with its joins.
- Every export can be the **whole sequence** or just the **selected composition**.

### Working faster
- Undo and redo (Ctrl/⌘+Z, Ctrl+Y or ⇧⌘Z).
- Keyboard shortcuts: press **?** in the app for the full list.
- **Restore last session** brings back your previous work, including uploads.
- **Export again** repeats your last export in one click.

---

## Using the app

1. Open the app link in a desktop browser.
2. Build your first composition in the side panel. Add more with **+** below the preview.
3. Click the round markers between compositions to choose how they join.
4. Click **Export** and choose MP4, PNG sequence or After Effects.

### Running the After Effects export
1. Unzip the downloaded folder somewhere it can stay.
2. In After Effects, choose **File → Scripts → Run Script File** and pick the `.jsx` file inside the folder.
3. Keep the other files next to the script, because it imports them as it builds.

Notes for the Live warp option:
- The script sets the project to **16 bits per channel**, which the warp maps need.
- If your project uses colour management, set **Project Settings → Color → Working Space** to **None** before running the script. The script warns you if this is needed.

---

## Browser support

Use a recent desktop version of **Chrome, Edge, Safari or Firefox**.

- MP4 export uses the browser's WebCodecs video encoder. It works best in Chrome and Edge.
- The app loads two small libraries from public CDNs (JSZip and mp4-muxer), so exports need an internet connection.

---

## Where your work is saved

Templates, presets, saved sessions and uploaded images and videos are stored **in your own browser**, for the web address you opened the app from.

- They are **not** shared with anyone else who opens the same link.
- They won't appear in a different browser, on a different computer, or at a different web address (for example, this GitHub link and the original claude.ai link have separate libraries).
- Clearing your browser's site data removes them.

---

## Updating the app

The whole app is the single `index.html` file.

1. Download the latest `index.html`.
2. In this repository, choose **Add file → Upload files**, drag in the new file, and commit.
3. GitHub Pages republishes the site within a minute or two.

### Hosting with GitHub Pages
1. In the repository, open **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**, then the **main** branch and the **/(root)** folder.
3. Save. The site address appears at the top of the Pages settings.

---

## Brand assets

This app contains S4C brand assets, including the S4C logo, the Cromlin artwork and the S4C typeface, which are built into `index.html`. These remain the property of S4C and are subject to their own terms and font licence. Check with the brand owner before making this repository or site public.

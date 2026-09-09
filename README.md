# Personal Portfolio Homepage

A static, responsive portfolio homepage built with HTML, CSS, JavaScript, Three.js, and Lucide Icons. No build step is required.

## Live Site

Your portfolio is deployed on **GitHub Pages** and runs 24/7 at:
```
https://YOUR_USERNAME.github.io/JARVIS_V1
```

See [DEPLOYMENT.md](DEPLOYMENT.md) for setup instructions.

## Local Development (Optional)

To test locally without GitHub:

```sh
python3 -m http.server 4173
```

Then open `http://127.0.0.1:4173/static/index.html`

The page imports Three.js, Lucide, and fonts from CDNs, so the first load needs an internet connection.

## Edit Your Content

Open `static/index.html` and search for `EDIT YOUR PERSONAL INFORMATION HERE`.

- Change `CONFIG.name`, `tagline`, `email`, and `accentColor` in the configuration object.
- Change `CONFIG.PORTFOLIO_PDF_URL` to your hosted PDF URL. This is the only value needed to connect the Vita screen and Portfolio document.
- The accent color is controlled by `--accent` and the `accentColor` configuration value. Keep the two values in sync when changing the color.
- The About section is marked with `EDITABLE CONTENT START/END` comments.

## Projects

Search for `ADD PROJECTS HERE` in the script. Add projects by copying an object in the `projects` array:

```js
{
  title: 'PROJECT TITLE',
  category: 'CATEGORY',
  year: '2026',
  image: '/images/project-placeholder.jpg',
  description: 'PROJECT DESCRIPTION',
  link: '#'
}
```

The current visual cards are procedural placeholders so there are no broken image requests. The `image` field is ready for a future image renderer.

## Documents

Search for `ADD DOCUMENTS HERE`. Add or remove objects in the `documents` array:

```js
{
  title: 'Portfolio',
  type: 'PDF',
  description: 'Selected creative work',
  url: CONFIG.PORTFOLIO_PDF_URL,
  icon: 'file-text'
}
```

PDFs open in the full-screen modal viewer. Other document types follow their URL in a new browser navigation.

## Replace The Vita Model

The current PS Vita is a lightweight procedural Three.js model with a body, illuminated screen, analog sticks, buttons, D-pad, lighting, shadow, damping, idle motion, and raycast screen interaction. This keeps the page self-contained and fast.

To replace it with a GLB later:

1. Put the file at `public/models/ps-vita.glb` (or another hosted URL).
2. Import `GLTFLoader` from the Three.js examples module in the module script.
3. Replace the block marked `Procedural Vita model` with `loader.load('/models/ps-vita.glb', ...)` and add the loaded scene to `vita`.
4. Keep the loaded screen mesh tagged with `userData.isScreen = true`, or update the raycast condition to match the model's screen node.

## Accessibility And Performance

The page includes keyboard focus states, semantic navigation, labelled controls, Escape-to-close PDF behavior, reduced-motion support, touch dragging, capped device pixel ratio, and low-cost procedural geometry. Replace placeholder labels and links before publishing.

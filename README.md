# Kawsar — Editorial Portfolio

A responsive single-page graphic design portfolio, redesigned with oversized typography, a dark vector-art hero, handwritten accents, fine grid lines, and light editorial sections. Built with React, Tailwind CSS, Framer Motion, Inter, and Caveat.

The layout takes visual direction from Neiden (https://neiden.framer.media/). The code, vector background, concept artwork, copy, and branding here are specific to this portfolio. No Neiden image assets, client claims, or testimonials are included.

## Update the existing GitHub / Vercel website

1. Extract the ZIP.
2. Open the existing GitHub repository.
3. Choose Add file > Upload files.
4. Upload the extracted `src` and `public` folders and the top-level files. Keep `package.json` at the repository root.
5. Commit the changes to the branch connected to Vercel.
6. Wait for the new deployment in Vercel to reach Ready.

Use these Vercel settings if needed:

- Framework: Vite
- Root directory: ./
- Install command: npm install
- Build command: npm run build
- Output directory: dist

No environment variables are required. A live Vercel deployment has not been modified by this local package.

## Run locally

Install Node.js 22 LTS or newer, then run:

    npm install
    npm run dev

Open the Local address printed in the terminal. Keep the terminal open while previewing.

Alternatively, the project includes a pnpm 11.25.0 lockfile:

    pnpm install
    pnpm dev

## Build for hosting

    npm run build

The static site is generated in `dist/`. To preview that build:

    npm run preview

## Add your real projects

Project content is separated into `src/data.js`.

1. Put an image, for example `my-brand.jpg`, inside `public/projects/`.
2. Open `src/data.js`.
3. Replace one sample project or add a new project entry with a unique `id`.
4. Set `image` to `/projects/my-brand.jpg` and `concept` to `false` for real portfolio work.
5. Update the title, category, type, description, and deliverables.

Example project entry:

    {
      id: 'my-brand',
      title: 'My Brand Project',
      type: 'Brand identity & packaging',
      category: 'Branding',
      image: '/projects/my-brand.jpg',
      imageAlt: 'Brand identity and packaging design for My Brand',
      concept: false,
      description: 'A short description of the brief, your approach, and the finished design.',
      deliverables: 'Logo design / Brand guidelines / Packaging'
    }

Filters and project counts update automatically from the project entries. Real images appear both in the grid and the project dialog. An unavailable image shows a clear fallback message. For consistent thumbnails, use high-resolution JPG, PNG, or WebP images with important content near the center; cards crop to fill the frame.

The six included sample projects remain explicitly labeled concepts until replaced. Do not represent the sample artwork as completed client work.

## Other edits

- Contact email: `EMAIL` in `src/data.js`.
- Biography, experience, services, and process: `src/main.jsx`.
- Colors, type, spacing, and responsive layouts: `src/styles.css`.
- Original sample artwork: `src/Artwork.jsx` and `src/artwork.css`.
- Page title and search description: `index.html`.
- CV: replace `public/md-kawsar-ahmed-cv.pdf` with a PDF of the same filename.

## Accessibility and behavior

Includes a skip link, semantic sections, keyboard-accessible navigation and service disclosures, category filters, project dialogs with focus management, Escape-to-close behavior, reduced-motion preferences, smooth scrolling, and responsive layouts. Contact links open the visitor's email app; no form submissions or backend are used.

## Fonts and CV

Inter is bundled through @fontsource/inter. Caveat is bundled in `public/fonts/` together with its SIL Open Font License.

The professional-only CV retains career, education, skills, city, phone, and the email selected for this portfolio. Home addresses, family details, date of birth, marital status, blood group, and personal interests are omitted.

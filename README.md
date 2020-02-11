# hugo-tailwindcss-starter

A Starter theme for Hugo with TailwindCSS. Enjoy creating your own theme with Tailwind!

## Minimum Hugo version
Hugo version 0.60.0 or higher is required.

## Installation
You can download and unpack the theme manually from Github or use git to clone the repo.

From the root of your site:
```shell
git clone https://github.com/javifm86/hugo-tailwindcss-starter.git themes/tailwindcss
```

If you use git on your site, add the theme as submodule.
```shell
git submodule add https://github.com/javifm86/hugo-tailwindcss-starter.git themes/tailwindcss
```

Go to theme folder and install dependencies with npm:
```shell
cd themes/tailwindcss
npm install
```

## Developing your theme

### HTML
Start editing and creating html files on `layouts` folder. You can use Tailwind classes based on your `tailwind.config.js` file.

### CSS
Development npm script:

```shell
npm run css:watch
```

Go to `themes/tailwindcss/static-src/css/styles.css` and start adding css styles. When file is saved the task generates `styles.css` on `themes/tailwindcss/static/css/`. You can customize default Tailwind config editing `tailwind.config.js` file.

If you don´t want the watch task, you can run just: `npm run css:build:dev` each time you want to refresh your `styles.css`.

## Build for production
Tailwind is compiled using PostCSS. You can see `postcss.config.js`, PurgeCSS + Autoprefixer + cssnano are included as build
process for final CSS. By default, folders included for `PurgeCSS` are:

- `"../../content/**/*.md"`: All markdown files for Hugo site (Note: markdown files out from themes folder).
- `"./layouts/**/*.html"`: HTML files used in theme.

You can change them or add as many paths as needed. Build npm script:

```shell
npm run css:build:prod
```

And final `styles.css` file optimized for production is generated on `themes/tailwindcss/static/css/folder`.
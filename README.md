# Résumé

Hello! My name is Lucas and this is my resumé repository. 

This resume was built upon the [Universal Resumé Template](https://github.com/WebPraktikos/universal-resume
), although it was modified to a different styling using TailwindCSS.
You can also fork/import this project and use it with your own information to build your own Resumé (:

I'm going to leave bellow the original instructions to import and run the project if you want to make your own version of it. 
Keep in mind, thought, that I do not authorize you to reuse any of my information on your resume if you choose to fork this repository (:

How to run it
---------

Navigate to the base directory:

```
cd universal-resume
```

Install the dependencies:

```
npm install
```

Start the development server:

```
npm run serve
```

Only generate CSS that is used on the page which results in a much smaller file size:

```
npm run build
```

Starting Point
---------

`docs/index.html` is the main content file. By copying HTML: add pages, sections, subsection, and other parts.

`npm run build` will make the **docs** directory ready for drag-n-drop to, for example, https://app.netlify.com/drop (free registration required beforehand).

Also, with additionally running `git add docs/styles.css -f` and committing changes, it’s ready for push to GitHub and integration with GitHub Pages. GitHub Pages are free for  public repositories. Under your repository name, not profile, click “Settings” and enable GitHub Pages by navigating to: `Options → GitHub Pages → Source → /docs`.

Tailwind CSS
---------

Tailwind CSS is a highly customizable, low-level CSS framework that gives you all of the building blocks you need to build bespoke designs without any annoying opinionated styles you have to fight to override. It has a great [documentation](https://tailwindcss.com/docs/installation).

Custom CSS
---------

Code from `tailwind.config.js` and `tailwind.css` transpiles to `docs/style.css`.

Here is the default tailwind config: [defaultConfig.stub.js](https://github.com/tailwindcss/tailwindcss/blob/master/stubs/defaultConfig.stub.js), and here’s the additional information from the Tailwind documentation: [theme](https://tailwindcss.com/docs/theme/#app).

If you want to change CSS in a classical way, add a class to the HTML element and write the CSS inside `tailwind.css`.

Balanced Columns
---------

Removing `col-fill-auto` class will make both columns equally tall. Moreover, removing `md:h-letter` and `md:h-letter-col` classes will eliminate fixed proportions of the letter or A4 page — thereby removing unnecessary vertical space when displaying short columns.

A4 Size Variant
---------

Change the default (letter) size to A4:

**1.** Inside `docs/index.html`, replace every `-letter` with `-a4`.

**2.** Inside `tailwind.config.js`, uncomment code block below `/* For A4 size */` and then comment code block below `/* For Letter size */`

**3.** Inside `tailwind.css`, comment code below `/* For Letter size */` and uncomment code below `/* For A4 size */`

**Important:** Too much content on one page will break the page in the form of additional columns.

Printing
---------

### Chrome

Right-click → Print.  
Also, choose the **Save as PDF** option if needed.

By expanding **More Settings**, change **Page Size** to A4 or Letter.

### Firefox

File → Print.

Choose A4 or Letter size by navigating to **Properties → Advanced → Paper Size**.

### Adobe Acrobat Reader

File → Print.

By clicking on the **Page Setup** button, you are taken to the window with A4 and Letter options.

Blocking Search Engines
---------

Disable search engine indexing by adding the following code to the `<head>`:

```html
<meta name="robots" content="noindex">
```

Language Support
---------

With [FiraGO](https://github.com/bBoxType/FiraGO) typeface, this résumé supports the following scrips: Latin, Cyrillic, Greek, Vietnamese, Arabic, Thai, Georgian, Devanagari, and Hebrew.

If you want to significantly speed up font loading time, find out what fonts you are using (under developer tools network panel) and add them to the `head` like so:

```html
<link rel="preload" href="./fonts/FiraGO-Regular.latin.woff2" as="font" crossorigin="anonymous">
```

License
---------

NonCommercial-ShareAlike 1.0 Generic (CC NC-SA 1.0)  
https://creativecommons.org/licenses/nc-sa/1.0/

### You are free to:

Share — copy and redistribute the material in any medium or format  

Adapt — remix, transform, and build upon the material

### Under the following terms:

NonCommercial — You may not use the material for commercial purposes.

ShareAlike — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.

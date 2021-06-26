# compareo_sass - SCSS-based UI build upon 7-1 architecture

This is the UI part of the compareo app.

## Features

- Node.js based SASS project
- 7-1 architecture (folder structure)
- includes Dart Sass scripts for creating bundled CSS and compressed CSS files
- implements new @use and @forward SASS module system (replaces @import)
- uses Font Awesome 5 icon library
- includes demo pages in "src/"-folder

## What's included?
Overview of folders structure within this project. All subfolders withing the "scss" folder follow the 7-1 architecture. The "src" folder contains the generated CSS output files as well as a bunch of html-files for demonstration purposes.

    .
    ├── scss
    │   ├── abstracts           # Functions, Mixins and global Variables
    │   ├── base                # Base, Reset, Typography and scrollbar configuration
    │   ├── components          # Elements such as Buttons, Badges, Tables, ...
    │   ├── layout              # Grid, Header, Navigation, Logo, Forms, ... 
    │   ├── pages               # Single Pages that require different layouts and independent CSS
    │   ├── themes              # empty (can be used for creating multiple themes)
    │   ├── vendors             # 3rd party libraries (Font Awesome and include-media)
    │   └── main.scss           # File that imports all subfolder content, is used for compiling CSS
    └── src
        ├── assets
        │   ├── css             # Output directory for all compiled CSS files 
        │   └── ...
        ├── create.html         # Demo of form and flyout menu
        ├── details.html        # Demo of project details page
        ├── index.html          # Demo of projects overview page
        ├── login.html          # Demo of login page
        └── register.html       # Demo of registration page

## Technologies

This project utilizes the following Technologies / Node Packages:
- Node.js
- dart-sass
- fontawesome

## Getting started

To get this project up and running, follow these steps:

### Prerequisites

- Node.js 14.17.0+
- IDE (preferably Visual Studio Code)

### Setup

1. Clone this repository
2. At the root directory, install required packages by running:

```
npm install
```

3. That's it! Now you have a couple of options to work with the existing code (all following code snippets are dart-sass commands):

- If you like to change the UI and have the SCSS files automatically recompiled to the CSS found in the "src/assets/css/" folder, run:

```
npm run watch-app
```

- If you like to simply compile the SCSS files to the CSS in the "src/assets/css/" folder, run:

```
npm run build-app
```

- If you like to compile the SCSS files to compressed CSS in the "src/assets/css/" folder, run:

```
npm run compress-app
```
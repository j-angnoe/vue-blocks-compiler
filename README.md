# Vue block compiler

Compiles a vue-blocks file into a standalone build.



# Usage

[NODE_ENV=production] vuebc [vue-blocks-file.html] -o [output-directory]

It will create:
- A vue file for each template[component]
- A vue file for each template[url]
- A vue file for each template[src]
- routes.js
- index.js
- index.html - which is the original file stripped of all the vue-blocks.

It will minify the files if you prepend NODE_ENV=production to the command.

# Pre-requisites:
You need to `npm install --save babel-plugin-transform-runtime` in your project.
Make sure the output directory exists.

# Example:

vuebc files/my-app.html -o build/my-app

Afterwards you can go open build/my-app/index.html with the browser.




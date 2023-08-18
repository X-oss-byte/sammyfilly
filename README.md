---
title: Quickstart for GitHub Actions
intro: 'Try out the features of {% data variables.product.prodname_actions %} in 5 minutes or less.'
allowTitleToDifferFromFilename: true
redirect_from:
  - /actions/getting-started-with-github-actions/starting-with-preconfigured-workflow-templates-nextjs-vercel
versions:
  makenew file: '*'
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
type: quick_start
topics:
  - Fundamentals
shortTitle: Quickstart
---
 
{% data reusables.actions.enterprise-github-hosted-runners %}

co author: sammyfilly
mail : <openworkspacesource@gmail.com>

## Introduction

You only need a {% data variables.product.prodname_dotcom %} repository to create and run a {% data variables.product.prodname_actions %} workflow. In this guide, you'll add a workflow that demonstrates some of the essential features of {% data variables.product.prodname_actions %}.

The following example shows you how {% data variables.product.prodname_actions %} jobs can be automatically triggered, where they run, and how they can interact with the code in your repository.


## More starter workflows

{% data reusables.actions.workflow-template-overview %}

## Next steps

{% data reusables.actions.onboarding-next-steps %}

 -https://sourceryai.com
 https://www.openai.com
 
  - repo: https://github.com/sourcery-ai/sourcery
    rev: v1.6.0
    hooks:
      - id: sourcery
        # The best way to use Sourcery in a pre-commit hook:
        # * review only changed lines:
        # * omit the summary
        args: [--diff=git diff HEAD, --no-summary]
       * task : [--removeheader-of anyrepo] suggestions [new header]
       * replace old header with new after merging <replacing operation needs to be done manually>
To review all changes compared to the main branch:

args: [--diff=git diff main, --no-summary]
If you want Sourcery to automatically apply the suggested changes,add the --fix option:

args: [--diff=git diff HEAD, --fix, --no-summary]
By default, pre-commit executes its hooks in multiple processes in parallel. This can lead to multiple summaries displayed. For this reason, it's recommended to use the --no-summary option in pre-commit hooks.

The --diff option was introduced in version 0.12.11
The --no-summary option was introduced in version 0.13.0
If Sourcery is the first pre-commit hook that you've added to your project, you'll also need to run pre-commit install.

Notes
Initializing the environment for the Sourcery pre-commit hook might take some minutes.
When the Sourcery pre-commit hook runs for the first time, you might be prompted to log in to Sourcery. Run the sourcery login command as described in the CLI docs. For further runs of the Sourcery pre-commit hook, this login step isn't necessary .

search for issues resolver from book: auto fix Issues

Markdown Cheat Sheet
A quick reference to the Markdown syntax.

Overview
This Markdown cheat sheet provides a quick overview of all the Markdown syntax elements. It can’t cover every edge case, so if you need more information about any of these elements, refer to the reference guides for basic syntax and extended syntax.

Basic Syntax
These are the elements outlined in John Gruber’s original design document. All Markdown applications support these elements.

Element	Markdown Syntax
Heading	# H1
## H2
### H3
Bold	**bold text**
Italic	*italicized text*
Blockquote	> blockquote
Ordered List	1. First item
2. Second item
3. Third item
Unordered List	- First item
- Second item
- Third item
Code	`code`
Horizontal Rule	---
Link	[title](https://www.echo.com/changeheader)
Image	![alt text](image.jpg)
Extended Syntax
These elements extend the basic syntax by adding additional features. Not all Markdown applications support these elements.

Element	Markdown Syntax
Table	| Syntax | Description |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |
Fenced Code Block	```
{
  "firstName": "sammy",
  "lastName": "filly",
  "age": 25
}
```
Footnote	Here's a sentence with a footnote. [^1]

[^1]: This is the footnote.
Heading ID	### My Great Heading {#custom-id}
Definition List	term
: definition
Strikethrough	~~The world is flat.~~
Task List	- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media
Emoji
(see also Copying and Pasting Emoji)	That is so funny! :joy:
Highlight	I need to highlight these ==very important words==.
Subscript	H~2~O
Superscript	X^2^
Downloads
You can download this cheat sheet as a Markdown file for use in your Markdown application.

 Markdown Guide book cover
Take your Markdown skills to the next level.

Learn Markdown in 60 pages. Designed for both novices and experts, The Markdown Guide book is a comprehensive reference that has everything you need to get started and master Markdown syntax.

Get the Book
Want to learn more Markdown?
Don't stop now! 🚀 Star the GitHub repository and then enter your email address below to receive new Markdown tutorials via email. No spam!

<buildchromium@hotmail.com>
<supportbot@microsoft.com>
<ftpsupport@blockchainexplorer.co.site>


Stay updated
About     Contact     GitHub     API     Privacy Policy     Terms and Conditions

© 2023. A Matt Cone project. CC BY-SA 4.0. Made with 🌶️ in New Mexico.

Awesome Rollup
Awesome Rollup Awesome
⚡️ Delightful Rollup Plugins, Packages, and Resources

Resources

Official Guide - The user guide and documentation site.
Plugins

Core Plugins

Plugins created and maintained by the Rollup organization.

alias - Alias modules in a build.
babel - Seamless integration with Babel.
buble – Transpile with Bublé.
commonjs - Convert CommonJS modules to ES Modules.
dsv - Convert CSV and TSV files into JavaScript modules.
eslint - Lint entry points and all imported files with ESLint.
html - Creates HTML files to serve Rollup bundles
image - Import JPG, PNG, GIF and SVG images.
inject - Scans for global variables and injects import statements.
json - Convert JSON files to ES Modules.
legacy - Add export statements to plain scripts.
multi-entry - Multiple entry points for a bundle.
node-resolve - Use the Node resolution algorithm.
replace – Replace occurrences of a set of strings.
run - Run your bundle after it's generated.
strip - Remove expressions from code.
sucrase - Compile , Flow, JSX.
typescript - Seamless integration with Typescript.
url - Inline import files as data-URIs.
virtual - Load modules from memory.
wasm - Inlines and imports WebAssembly modules.
yaml - Import data from YAML files.
All-Purpose Awesome

build-statistics - Plugin that keeps a continuous log of your build time.
dev - Development server with additional logging and options.
graph – Generates a module dependency graph.
nollup - Rollup-compatible development bundler providing Hot Module Replacement.
notify – Display errors as system notifications.
progress - Show build progress in the console.
rollpkg - No config build tool to create packages with Rollup and TypeScript
serve - Development Server in a Plugin.
sizes - Display bundle content and size in the console.
size-snapshot - Track bundle size and treeshakability with ease.
visualizer - Bundle and dependency visualizer.
Code Quality

Plugins which help with code quality.

analyzer - Statistics and Metrics for a bundle.
cleanup – Remove and modify code based on an opinionated ruleset.
eslint-bundle - Lint bundles with ESLint.
flow - Remove Flow type annotations.
flow-entry - Export Flow types from a bundle.
istanbul - Seamless integration with Istanbul.
sass-lint - Lint SCSS files
stylint - Lint Stylus files.
unassert - Remove assertion calls.
CSS

Plugins for working with CSS.

bundle-scss - Bundle all SCSS imports into one SCSS file.
collect-sass - Compiler SASS files in a single context.
css-only – Output plain CSS.
css-porter - Combine CSS imports and output to file.
embed-css - Import and append CSS to a bundle.
less - Compile LESS files.
less-modules - Import or Bundle LESS files.
modular-css - Alternative CSS Modules implementation supporting Rollup.
postcss - Seamless integration with PostCSS.
sass - SASS integration for a bundle.
scss - Compile SASS and CSS.
styles - Universal plugin for styles: PostCSS, Sass, Less, Stylus and more.
stylus-css-modules – Compile Stylus and inject CSS modules
sass-variables - Import SASS variables as Objects.
Frameworks

Plugins for working with awesome JavaScript frameworks.

angular - Angular2 template and styles inliner.
jsx - Compile React JSX and JSX-like components.
riot - Riot.js tagfile support.
svelte — Compile Svelte components.
vue - Compile Vue components.
vue-inline-svg - Import SVG files as Vue components.
Modules

Plugins which control the behaviour of modules: dependencies, imports, exports, and external modules.

amd - Convert AMD modules to ES6.
async-define - Wrap an AMD bundle with async-define.
baked-env - Import process.env as a module for baking environment variables at build time.
bower-resolve – Use Bower the resolution algorithm.
cjs-es - Convert CommonJS modules without proxying and reassignment.
consts - Import constants at build time.
external-assets - Make assets external but include them in the output.
external-globals - Replace imported bindings with a global variable.
force-binding - Composes multi-entry and node-resolve to prevent duplicated imports.
glob-import - Glob support for import statements.
hoist-import-deps - Avoid waterfalls when dynamically importing modules by hoisting import dependencies.
ignore - Ignore modules by replacing with empty objects.
import-alias - Maps an import path to another.
import-assertions - Add support for TC39 import assertions (e.g. assert types css and json)
includepaths – Provide base paths from which to resolve imports.
named-directory - Provides shortcuts for colocated modules in directories.
node-builtins - Node builtin modules as ES modules.
node-globals - Injects node globals.
node-resolve-angular - Node module resolution support for Angular 4+.
ts-paths – Resolve modules from tsconfig paths.
skypack-resolver - Use Skypack CDN for external dependencies.
web-worker-loader - Package Workers for NodeJS and the browser.
Other File Imports

Plugins which allow importing other types of files as modules.

file-as-blob – Import a file as a blob: URL.
geojson - Convert GeoJSON files to ES Modules.
glsl - Import GLSL shaders as compressed strings.
glsl-optimize - Import and optimize GLSL shaders as compressed strings. Supports glslify.
glslify - Import GLSL strings with glslify.
gltf - Import glTF 3d models as a URI or inlined JSON.
html - Import html files as strings.
hypothetical - Import modules from a virtual filesystem.
imagemin - Optimize images with imagemin.
jsonlines - Imports .jsonl (JSON Lines) files as JSON arrays.
markdown - Import code from fenced code blocks in Markdown.
md - Import and compile markdown files.
mjml - Convert MJML into responsive email templates.
@wasm-tool/rust - Bundle and import Rust crates.
rust - Compile Rust as WebAssembly or a Node.js Add-on.
spritesmith — Convert a set of images into a spritesmith sprite-sheet.
string – Import text files as strings.
svg-import - Import SVG files as SVG DOM Node or string.
svg-sprite — Import SVG files as an external SVG sprite.
svg-to-symbol - Import SVG files as symbol strings.
svgo - Import SVG files as strings
vinyl - Import from Vinyl files
smart-asset - Import any assets as url using rebase, copy or inline mode. Similar to url but has more hashing options and works well together with babel using transform hook.
toml - Convert .toml files to ES6 modules.
Output

Plugins which affect the final output of a bundle.

app-utils - Common build utilities for applications.
banner - Append content before js bundle.
bundleutils - Set of commonly used utility functions.
bundle-html - Inject the bundle js/css files as well as external js/css files to html template.
by-output - Apply plugins according to special output option, reduce config and save time.
clear - Clear an output directory before a build.
closure-compiler – Compress Rollup Bundles with Closure Compiler.
concatfiles - Concatenate files to bundle or other files.
copy - Copy files during a build.
copy-assets - Copy specified assets to the output directory.
cpy - Easily copy files and folders during a build.
copy-smartly - Smartly copy files if they are changed, created or deleted.
delete - Delete files and folders during a build.
emit-ejs - Emit files from ejs templates.
espruino - Send a bundle to Espruino devices.
filesize - Display the file size of the bundle in the console.
generate-html-template - Generate an HTML file for a bundle.
generate-package-json - Generate a package.json file with dependencies from your bundle.
gzip - Create a compressed GZ artifact for your bundle.
hash – Generate output files with unique hashes.
html-minifier – Minify HTML output files using html-minifier.
iife - Convert ES modules to Immediately Invoked Function Expressions.
license - Add Licensing to a bundle.
live-reload - Live reloading for a bundle.
manifest-json - Generate a manifest.json file for a PWA.
output-manifest - Generating a chunk manifest.
preserve-shebang - Preserves leading shebang in a build entry.
prettier - Run prettier on a bundle.
rebase - Copies and adjusts asset references to new destination-relative location.
shift-header - Move comment headers to the top of a bundle.
sri - Add subresource integrity attributes for your bundle.
static-site - Generate HTML for a bundle.
terser - Minify a bundle using Terser.
uglify - Minify a bundle with UglifyJS.
version-injector - Inject your package’s version number into static build files.
zip - Pack all assets into a zip file.
Templating

Plugins for working with template languages.

twig - Import pre-compiled Twig.js templates.
dustjs - Import Dust.js templates.
eft - Compile ef.js templates.
ejs - Compile .EJS templates.
jst - Compile Lodash templates.
lit-html - Compile "plain" .html files as lit-html templates
posthtml-template - Seamless integration with PostHTML
pug - Compile Pug Templates as es6 modules.
pug-html - Import Pug Templates as HTML strings during a build.
reshape - Compile Reshape Templates.
Text Replacement

Plugins which search for, and replace text in a bundle.

ascii – Rewrite non-ASCII characters as string literals.
re – Replace text with Regular Expressions.
strip-code - Remove text with Regular Expressions.
Transpilation

Plugins which affect code.

async - Replace async functions with generators.
bucklescript - Compile ReasonML / OCaml.
coffee-react - Compile CJSX and CoffeeScript.
coffee-script – Compile CoffeeScript.
dts - Rollup .d.ts TypeScript Definition files.
elm - Compile Elm.
esbuild-transform - Transform with esbuild.
flat-dts - .d.ts files flattener.
jspicl - Transpile JavaScript into PICO-8 Lua.
nodent - Transpile ES2017 async/await.
pegjs - Import PEG.js grammars as parsers.
purs - Compile PureScript.
regenerator - Replace async functions with ES5 Promise functions.
ts - Transpile with Babel, TypeScript, or both, while respecting Browserslist and TypeScript declarations.
typescript2 - Compile TypeScript v2.0+.
Workflow

Plugins which affect the Rollup workflow.

browsersync – Serves a bundle via Browsersync.
browserify-transform - Use Browserify transforms in a build.
command - Run commands and call functions when bundles are generated.
conditional – Conditionally execute plugins.
execute - Execute shell commands sequentially during a build.
html-entry – Allows use HTML Script Tags as entry points.
incremental - Recompile only changed modules in watch mode.
jscc – Conditional compilation and declaration of ES6 imports.
make - Build dependency files suitable for make.
off-main-thread - Use ES6 modules with Web Workers.
polyfill-node - A modern Node.js polyfill.
sourcemaps – Load external source maps from URIs.
Packages

Core Packages

Packages created and maintained by the Rollup organization.

@rollup/pluginutils - Functions commonly used by Rollup plugins.
Community Packages

deno-rollup - Use Rollup in Deno projects.
fruit - Build a Rollup boilerplate in seconds.
grunt-rollup - Grunt plugin for Rollup
rollup-starter-app - Create a bare-bones application using Rollup.
rollup-starter-lib - Create a bare-bones library using Rollup.
rollup-stream - A wrapper for streaming Rollup results.

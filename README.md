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


{% data reusables.actions.workflow-template-overview %}

## Next steps

{% data reusables.actions.onboarding-next-steps %}

 -<https://sourceryai.com>
 <https://www.openai.com>
 
  - repo: https://github.com/sourcery-ai/sourcery
    rev: v1.6.0
    hooks:
      - id: sourcery
        # The best way to use Sourcery in a pre-commit hook:
        # * review only changed lines:
        # * omit the summary
        args: [--diff=git diff HEAD, --no-summary]
       * task : [--removeheader-of anyrepo] suggestions [new header] not GitHub header and external link required for building website 
      
         * old header: not found/needed
        * new header :acess body and avoid what happened to old header in feature
merge: merging <replacing operation needs to be done manually>
To review all changes compared to the main branch:

args: [--diff=git diff main, --no-summary]
If you want Sourcery to automatically apply the suggested changes,add the --fix option:

args: [--diff=git diff HEAD, --fix, --no-summary]
By default, pre-commit executes its hooks in multiple processes in parallel. This can lead to multiple summaries displayed. For this reason, it's recommended to use the --no-summary option in pre-commit hooks.

The --diff option was introduced in version 0.12.11
The --no-summary option was introduced in version 0.13.0
If Sourcery is the first pre-commit hook that you've added to your project, you'll also need to run pre-commit install.

**
__________________
Code Splitting ​

For code splitting, there are cases where Rollup splits code into chunks automatically, like dynamic loading or multiple entry points, and there is a way to explicitly tell Rollup which modules to split into separate chunks via the output.manualChunks option.

To use the code splitting feature to achieve the lazy dynamic loading (where some imported module(s) is only loaded after executing a function), we go back to the original example and modify src/main.js to load src/foo.js dynamically instead of statically:

js
// src/main.js
export default function () {
	import('./foo.js').then(({ default: foo }) => console.log(foo));
}
Rollup will use the dynamic import to create a separate chunk that is only loaded on demand. In order for Rollup to know where to place the second chunk, instead of passing the --file option we set a folder to output to with the --dir option:

shell
rollup src/main.js -f cjs -d dist
This will create a folder dist containing two files, main.js and chunk-[hash].js, where [hash] is a content based hash string. You can supply your own naming patterns by specifying the output.chunkFileNames and output.entryFileNames options.

You can still run your code as before with the same output, albeit a little slower as loading and parsing of ./foo.js will only commence once we call the exported function for the first time.

shell
node -e "require('./dist/main.js')()"
If we do not use the --dir option, Rollup will again print the chunks to stdout, adding comments to highlight the chunk boundaries:

js
//→ main.js:
'use strict';

function main() {
	Promise.resolve(require('./chunk-b8774ea3.js')).then(({ default: foo }) =>
		console.log(foo)
	);
}

module.exports = main;

//→ chunk-b8774ea3.js:
('use strict');

var foo = 'hello world!';

exports.default = foo;
This is useful if you want to load and parse expensive features only once they are used.

A different use for code-splitting is the ability to specify several entry points that share some dependencies. Again we extend our example to add a second entry point src/main2.js that statically imports src/foo.js just like we did in the original example:

js
// src/main2.js
import foo from './foo.js';
export default function () {
	console.log(foo);
}
If we supply both entry points to rollup, three chunks are created:

shell
rollup src/main.js src/main2.js -f cjs
will output

js
//→ main.js:
'use strict';

function main() {
	Promise.resolve(require('./chunk-b8774ea3.js')).then(({ default: foo }) =>
		console.log(foo)
	);
}

module.exports = main;

//→ main2.js:
('use strict');

var foo_js = require('./chunk-b8774ea3.js');

function main2() {
	console.log(foo_js.default);
}

module.exports = main2;

//→ chunk-b8774ea3.js:
('use strict');

var foo = 'hello world!';

exports.default = foo;
Notice how both entry points import the same shared chunk. Rollup will never duplicate code and instead create additional chunks to only ever load the bare minimum necessary. Again, passing the --dir option will write the files to disk.

You can build the same code for the browser via native ES modules, an AMD loader or SystemJS.

For example, with -f es for native modules:

shell
rollup src/main.js src/main2.js -f es -d dist
html
<!doctype html>
<script type="module">
	import main2 from './dist/main2.js';
	main2();
</script>
Or alternatively, for SystemJS with -f system:

shell
rollup src/main.js src/main2.js -f system -d dist
Install SystemJS via

shell
npm install --save-dev systemjs
And then load either or both entry points in an HTML page as needed:

html
<!doctype html>
<script src="node_modules/systemjs/dist/s.min.js"></script>
<script>
	System.import('./dist/main2.js').then(({ default: main }) => main());
</script>
See rollup-starter-code-splitting for an example on how to set up a web app that uses native ES modules on browsers that support them with a fallback to SystemJS if necessary.

*<https://nextjs.org>can assist in setting requirements for next job or previous 
Previous page
Javascript API
Next page
ES Module Syntax

ES Module Syntax
Importing
Named Imports
Namespace Imports
Default Import
Empty Import
Dynamic Import
Exporting
Named exports
Default Export
How bindings work
The following is intended as a lightweight reference for the module behaviors defined in the ES2015 specification, since a proper understanding of the import and export statements are essential to the successful use of Rollup.

Importing ​

Imported values cannot be reassigned, though imported objects and arrays can be mutated (and the exporting module, and any other importers, will be affected by the mutation). In that way, they behave similarly to const declarations.

Named Imports ​
Import a specific item from a source module, with its original name.

js
import { something } from './module.js';
Import a specific item from a source module, with a custom name assigned upon import.

js
import { something as somethingElse } from './module.js';
Namespace Imports ​
Import everything from the source module as an object which exposes all the source module's named exports as properties and methods.

js
import * as module from './module.js';
The something example from above would then be attached to the imported object as a property, e.g. module.something. If present, the default export can be accessed via module.default.

Default Import ​
Import the default export of the source module.

js
import something from './module.js';
Empty Import ​
Load the module code, but don't make any new objects available.

js
import './module.js';
This is useful for polyfills, or when the primary purpose of the imported code is to muck about with prototypes.

Dynamic Import ​
Import modules using the dynamic import API.

js
import('./modules.js').then(({ default: DefaultExport, NamedExport }) => {
	// do something with modules.
});
This is useful for code-splitting applications and using modules on-the-fly.

Exporting ​

Named exports ​
Export a value that has been previously declared:

js
const something = true;
export { something };
Rename on export:

js
export { something as somethingElse };
Export a value immediately upon declaration:

js
// this works with `var`, `let`, `const`, `class`, and `function`
export const something = true;
Default Export ​
Export a single value as the source module's default export:

js
export default something;
This practice is only recommended if your source module only has one export.

It is bad practice to mix default and named exports in the same module, though it is allowed by the specification.

How bindings work ​

ES modules export live bindings, not values, so values can be changed after they are initially imported as per this demo:

js
// incrementer.js
export let count = 0;

export function increment() {
	count += 1;
}
js
// main.js
import { count, increment } from './incrementer.js';

console.log(count); // 0
increment();
console.log(count); // 1

count += 1; // Error — only incrementer.js can change this
____________________
mage	![alt text](image.jpg)
Extended Syntax
These elements extend the basic syntax by adding additional features. Not all Markdown applications support these elements.

Element	Markdown Syntax
Table	| Syntax | Description |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |
Fenced Code Block	```
Notes
Initializing the environment for the Sourcery pre-commit hook might take some minutes.
When the Sourcery pre-commit hook runs for the first time, you might be prompted to log in to Sourcery. Run the sourcery login command as described in the CLI docs. For further runs of the Sourcery pre-commit hook, this login step isn't necessary .

search for issues resolver from book: auto fix Issues

(https://www.echo.com/changeheader)
any project created assign admin field to
{
  "firstName": "sammy",
  "lastName": "filly",
  "age": 25
}
mail : <buildchromium@hotmail.com
```

About     Contact us :<supportbot@microsoft.com>
 ftpsupport@blockchainexplorer.co.site
    GitHub     API     Privacy Policy     Terms and Conditions

© 2023. A Matt Cone project. CC BY-SA 4.0. Made with 🌶️ in New Mexico.

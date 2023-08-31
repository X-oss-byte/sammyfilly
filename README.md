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

## Creating your first workflow

1. Create a `.github/workflows` directory in  your repository on {% data variables.product.prodname_dotcom %} if this directory does not already exist.
1. In the `.github/workflows` directory, create a file named `github-actions-demo.yml`. For more information, see "[AUTOTITLE](/repositories/working-with-files/managing-files/creating-new-files)."
1. Copy the following YAML contents into the `github-actions-demo.yml` file:

   ```yaml copy
   name: GitHub Actions Demo
   {%- ifversion actions-run-name %}
   run-name: {% raw %}${{ github.actor }}{% endraw %} is testing out GitHub Actions 🚀
   {%- endif %}
   on: [push]
   jobs:
     Explore-GitHub-Actions:
       runs-on: ubuntu-latest
       steps:
         - run: echo "🎉 The job was automatically triggered by a {% raw %}${{ github.event_name }}{% endraw %} event."
         - run: echo "🐧 This job is now running on a {% raw %}${{ runner.os }}{% endraw %} server hosted by GitHub!"
         - run: echo "🔎 The name of your branch is {% raw %}${{ github.ref }}{% endraw %} and your repository is {% raw %}${{ github.repository }}{% endraw %}."
         - name: Check out repository code
           uses: {% data reusables.actions.action-checkout %}
         - run: echo "💡 The {% raw %}${{ github.repository }}{% endraw %} repository has been cloned to the runner."
         - run: echo "🖥️ The workflow is now ready to test your code on the runner."
         - name: List files in the repository
           run: |
             ls {% raw %}${{ github.workspace }}{% endraw %}
         - run: echo "🍏 This job's status is {% raw %}${{ job.status }}{% endraw %}."
   ```

1. Scroll to the bottom of the page and select **Create a new branch for this commit and start a pull request**. Then, to create a pull request, click **Propose new file**.

   ![Screenshot of the "Commit new file" area of the page.](/assets/images/help/repository/actions-quickstart-commit-new-file.png)

Committing the workflow file to a branch in your repository triggers the `push` event and runs your workflow.

## Viewing your workflow results

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.actions-tab %}
1. In the left sidebar, click the workflow you want to display, in this example "GitHub Actions Demo."

   ![Screenshot of the "Actions" page. The name of the example workflow, "GitHub Actions Demo", is highlighted by a dark orange outline.](/assets/images/help/repository/actions-quickstart-workflow-sidebar.png)
1. From the list of workflow runs, click the name of the run you want to see, in this example "USERNAME is testing out GitHub Actions."
1. In the left sidebar of the workflow run page, under **Jobs**, click the **Explore-GitHub-Actions** job.

   ![Screenshot of the "Workflow run" page. In the left sidebar, the "Explore-GitHub-Actions" job is highlighted with a dark orange outline.](/assets/images/help/repository/actions-quickstart-job.png)
1. The log shows you how each of the steps was processed. Expand any of the steps to view its details.

   ![Screenshot of steps run by the workflow.](/assets/images/help/repository/actions-quickstart-logs.png)

   For example, you can see the list of files in your repository:
   ![Screenshot of the "List files in the repository" step expanded to show the log output. The output for the step is highlighted with a dark orange highlight.](/assets/images/help/repository/actions-quickstart-log-detail.png)

The example workflow you just added is triggered each time code is pushed to the branch, and shows you how {% data variables.product.prodname_actions %} can work with the contents of your repository. For an in-depth tutorial, see "[AUTOTITLE](/actions/learn-github-actions/understanding-github-actions)."

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


Stay updated
About     Contact     GitHub     API     Privacy Policy     Terms and Conditions

© 2023. A Matt Cone project. CC BY-SA 4.0. Made with 🌶️ in New Mexico.
        self.force_slider = self._extracted_from_method_two_2("Force", DEFAULT_FORCE)

    # TODO Rename this here and in `method_one` and `method_two`
    def _extracted_from_method_two_2(self, label, arg1):
        result = Scale(self.parent, from_=1, to=10, orient=HORIZONTAL, label=label)
        result.pack()
        result.set(arg1)
        result.configure(background="white")
        return result
Explanation:¶

Do not Repeat Yourself (DRY) is an important tenet of writing clean, maintainable code. Duplicated code bloats the code base, making it harder to read and understand. It often also leads to bugs. Where changes are made in only some of the duplicated areas unintended behaviour will often arise.

One of the main ways to remove duplication is to extract the common areas into another method and call that. Sourcery can detect areas of duplicate code that are in different functions in the same class and extract them. It is recommended that you then rename the extracted function and any arguments that have not been automatically named. In the above example a suitable method name would be create_slider, and arg1 would be default_value.

Note that this refactoring only runs when a file is opened or saved - it does not get triggered whenever you change the code in a file.

Comprehension to Generator¶

Sourcery refactoring id: comprehension-to-generator¶

Description:¶

Replace unneeded comprehension with generator

Before:¶

hat_found = any([is_hat(item) for item in wardrobe])
After:¶

hat_found = any(is_hat(item) for item in wardrobe)
Explanation:¶

Functions like any, all and sum allow you to pass in a generator rather than a collection. Doing so removes a pair of brackets, making the intent slightly clearer. It will also return immediately if a hat is found, rather than having to build the whole list. This lazy evaluation can lead to performance improvements.

Note that we are actually passing a generator into any() so strictly speaking the code would look like this:

hat_found = any((is_hat(item) for item in wardrobe))
but Python allows you to omit this pair of brackets.

The standard library functions that accept generators are:

"all", "any", "enumerate", "frozenset", "list", "max", "min", "set", "sum", "tuple"
**for other important steps 
extract data from below link
<https://docs.sourcery.ai/Reference/Python/Default-Rules/comprehension-to-generator/>
=======

!DOCTYPE
<hmtl> 
echo : call body import from globe 
handle returned body 
return footer 
return links and everything linked to <hmtl>
>>>>>>> main


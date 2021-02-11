# The RSG Workshop Template

This repository is the Research Software Group's template for creating websites for workshops.

It is based on the The Carpentries' [Workshop Template][carp-workshop-template].

1. **Please _do not fork this repository directly on GitHub._** Instead, please use GitHub's
   "template" function following [the instructions below](#creating-a-repository) to copy this
   `workshop-template` repository and customize it for your workshop.

2. Please *do your work in your repository's `gh-pages` branch*, since that is what is
   [automatically published as a website by GitHub][github-project-pages].

## Creating a Repository

1.  Log in to GitHub.
    (If you do not have an account, you can quickly create one for free.)
    You must be logged in for the remaining steps to work.

2.  On this page (<https://github.com/southampton-rsg/workshop-template>),
    click on the green "Use this template" button (top right)

    ![the 'use this template' button on GitHub](fig/select-github-use-template.png?raw=true)

3.  Select the owner for your new repository (the southampton-rsg organisation).

4.  Choose a name for your workshop website repository.
    This name should have the form `YYYY-MM-DD-client-type`,
    e.g., `2016-12-01-southampton-swc`,
    where `YYYY-MM-DD` is the start date of the workshop, `southampton` is the client/location of the
    workshop, and `swc` is the type of the workshop. `swc` (Software Carpentry), `dc` (Data
    Carpentry workshop), or `crs` (Computational Research Skills).

    If your workshop is held online, then the respository name should have `-online` in the end.
    e.g., `2016-12-01-southampton-swc-online`

5.  Make sure the repository is public, leave "Include all branches" unchecked, and click
    on "Create repository from template".
    You will be redirected to your new copy of the workshop template respository.

6.  Your new website will be rendered at `https://southampton-rsg.github.io/YYYY-MM-DD-client-type`.

## Customizing Your Website (Required Steps)

There are two ways of customizing your website. You can either:

- edit the files directly in GitHub using your web browser
- clone the repository on your computer and update the files locally

### Updating the files on GitHub in your web browser

1.  Go into your newly-created repository,
    which will be at `https://github.com/southampton-rsg/YYYY-MM-DD-site-type`.

2.  Ensure you are on the gh-pages branch by clicking on the branch under the drop
    down in the menu bar (see the note below):

    ![](fig/select-gh-pages-branch.png?raw=true)

3.  Edit the header of `index.md` to customize the list of instructors,
    workshop venue, etc.
    You can do this in the browser by clicking on it in the file view on GitHub
    and then selecting the pencil icon in the menu bar:

    ![](fig/edit-index-file-menu-bar.png?raw=true)

    Editing hints are embedded in `index.md`,
    and full instructions are in [the customization instructions][customization].

    FIXME: remove curriculum, flavor features?
4.  Edit `_config.yml` to customize certain site-wide variables, such as: `carpentry` (to tell your
    participants the lesson program for your workshop), `curriculum` and `flavor` for the
    curriculum  taught in your workshop, and `title` (overall title for all pages).

    Editing hints are embedded in `_config.yml`,
    and full instructions are in [the customization instructions][customization].

5.  Edit the `schedule.md` file to edit the schedule for your upcoming workshop, and possibly the
    `who.md` file which describes who should attend, and the `intro.md` file if you need to change
    the introductory paragraph. These files are
    located in the `_includes` directory, make sure to choose the one from the appropriate `dc` (Data
    Carpentry workshop), `crs` (Computational Research Skills), or `swc`
    (Software Carpentry) subdirectory.

### Working locally

> Note: you don't have to do this, if you have already updated your site using the web interface.


If you are already familiar with Git, you can clone the repository to your desktop, edit `index.md`,
`_config.yml`, and `schedule.md` following the instruction above there, and push your changes back to the repository.

```shell
git clone https://github.com/your_username/YYYY-MM-DD-site-type
```

In order to view your changes once you are done editing, if you have bundler installed (see the
[installation instructions below](#installing-software)), you can preview your site locally with:

```shell
make serve
```
and go to <http://0.0.0.0:4000> to preview your site.

Before pushing your changes to your repository, we recommend that you also check for any potential
issues with your site by running:

```shell
make workshop-check
```

Once you are satisfied with the edits to your site, commit and push the changes to your repository.
A few minutes later, you can go to the GitHub Pages URL for your workshop site and preview it. In the example above, this is `https://gvwilson.github.io/2016-12-01-miskatonic`. The finished
page should look [something like this](fig/completed-page.png?raw=true).


## Optional but Recommended Steps


### Update your repository description and link your website

At the top of your repository on GitHub you'll see

~~~
No description, website, or topics provided. — Edit
~~~

Click 'Edit' and add:

1.  A very brief description of your workshop in the "Description" box (e.g., "Southampton University workshop, Dec. 2016")

2.  The URL for your workshop in the "Website" box (e.g., `https:/southampton-rsg.github.io/2016-12-01-southampton-swc`)

This will help people find your website if they come to your repository's home page.

### Update the content of the README file

You can change the `README.md` file in your website's repository, which contains these instructions,
so that it contains a short description of your workshop and a link to the workshop website.


## Additional Notes

**Note:**
please do all of your work in your repository's `gh-pages` branch,
since [GitHub automatically publishes that as a website][github-project-pages].

**Note:**
this template includes some files and directories that most workshops do not need,
but which provide a standard place to put extra content if desired.
See the [design notes][design] for more information about these.

Further instructions are available in [the customization instructions][customization].
This [FAQ][faq] includes a few extra tips (additions are always welcome)
and these notes on [the background and design][design] of this template may help as well.


## Creating Extra Pages

In rare cases,
you may want to add extra pages to your workshop website.
You can do this by putting either Markdown or HTML pages in the website's root directory
and styling them according to the instructions give in
[the lesson template][lesson-example].


## Installing Software

If you want to set up Jekyll so that you can preview changes on your own machine before pushing them
to GitHub, you must install the software described in the lesson example [setup
instructions](https://carpentries.github.io/lesson-example/setup.html#jekyll-setup-for-lesson-development).


[email]: mailto:team@carpentries.org
[carp-workshop-template]: https://github.com/carpentries/workshop-template
[customization]: https://carpentries.github.io/workshop-template/customization/index.html
[dc-site]: https://datacarpentry.org
[design]: https://carpentries.github.io/workshop-template/design/index.html
[faq]: https://carpentries.github.io/workshop-template/faq/index.html
[github-project-pages]: https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site
[issues]: https://github.com/carpentries/workshop-template/issues
[lesson-example]: https://carpentries.github.io/lesson-example/
[self-organized-workshop-form]: https://amy.carpentries.org/forms/self-organised/
[swc-site]: https://software-carpentry.org
[lc-site]: https://librarycarpentry.org

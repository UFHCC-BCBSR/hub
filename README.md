
## UFHCC BCB-SR Bioinformatics Wiki

The UFHCC BCB-SR Bioinformatics wiki is where we BCB-SR Bioinformatics members collaboratively document how to navigate bioinformatics in the UF Health Cancer Center (and beyond) from collaborating with the BCB-SR Bioinformatics unit, using the command line, finding gold-standard tools, and trouble-shotting common challenges.

This is the GitHub repository that stores all of the relevant code and content. The wiki is available at <https://ufhcc-bcbsr.github.io/wiki>

The site is built using [Wowchemy](https://wowchemy.com/), the [Wowchemy Project Documentation template](https://github.com/wowchemy/hugo-documentation-theme), and the [Hugo static site generator](https://gohugo.io/).

## Requesting updates to the wiki

### Create an issue

Go to <https://github.com/UFHCC-BCBSR/wiki/issues> and "create a new issue". Describe what information you would like documented on the wiki. You can suggest your own content if you just learned about a new tool or topic, or leave an open-ended request that we document best practices for a particular assay or analysis.

## Editing the wiki (for repo collaborators)

### Editing an existing page

All of the wiki content is stored in markdown files in the `content/docs/` directory.

* To edit from the GitHub repository find the associated page click the pencil icon to edit
* To edit from the website click the Edit this page link at the bottom of the page you want to edit and you’ll be redirected to the GitHub repository to edit

In both cases when you are done editing add a descriptive commit message at the bottom of the page, select `Commit directly to the main branch`, and click the `Commit changes` button. If you want someone else to look at your changes before they are added to the wiki you can select `Create a new branch for this commit and start a pull request` instead and click the `Propose changes` button and someone will review the changes before merging them into the wiki.

### Adding a new page 

1. In the GitHub repo navigate to the appropriate folder in `content/docs/` and click `Add file` and then `Create new file`.
2. Add the following YAML to the top of the page and edit the text of the `title` and `summary` fields to match the new page.

```yaml
---
title: "Hi-C Data Analysis"
summary: >
  Best Practies for Hi-C Data Analysis
---
```

3. Add the text for the page
4. A descriptive commit message at the bottom of the page, and select `Commit directly to the main branch` (if you don't want the changes reviewed) or `Create a new branch for this commit and start a pull request` (if you want the changes reviewed), and click the `Commit changes` or `Propose changes` button.

### Adding a new topic

1. In the GitHub repo navigate to the appropriate folder in `content/docs/` and click `Add file` and then `Create new file`
2. Type the name of the directory you want to create for the topic, then `/`, and then `_index.md`
3. Add the following text to the page and the text of the `title`, `summary`, and the paragraph description to match the new topic.

```
---
title: "Normalization Methods in Bioinformatics"
summary: >
  The importance of normalization methods in bioinformatics analysis
---

Normalization is a critical step in bioinformatics analysis whether for visualization or as implemented in differential analysis testing. 

{{< list_children >}}
```

4. Commit the changes as described above
5. You can now add a new page to the new topic

## License

All content is licensed [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/) and the Wowchemy infrastructure is licensed [MIT](https://mit-license.org/) by Wowchemy.

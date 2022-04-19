# OHBM Open Science Special Interest Group

[![Netlify Status](https://api.netlify.com/api/v1/badges/29ccff18-6595-4078-8f08-f20f482ec9eb/deploy-status)](https://app.netlify.com/sites/ossig/deploys)

The landing page of the OHBM Open Science special interest group (OSSIG).

## Run the website locally

1. Install hugo

See the instruction related to the operatiing system you are using on the [hugo documentation](https://gohugo.io/getting-started/installing/).

2. Fork and clone this repository

3. Run the site locally
```
hugo server
```

## Changing things
There's a wide variety of customizations that you can make to your Hugo Fresh landing page by modifying the `config.yaml` file that you downloaded. That file provides documentation for what the various config values represent.

We have added some extra section in there to easily modify the OSSIG team members, the sponsors...

If you want more ideas you can check the content of `themes/hugo-fresh/exampleSite/config.yaml`

New standalone pages should be added in the `content` folder by creating a file `content/newpage/index.md` whose content should be:

```markdown
---
title: "new page"
subtitle: "no really, this is a new page"
date: 2020-01-26T21:55:26+01:00
draft: false
sidebar: false # true or false to display the sidebar
sidebarlogo: fresh-white-alt # From (static/images/logo/)
include_footer: true
---

here write the actual content of your page using markdown.

```

### Members and past members

Currently, the details about current team members (names, affiliations, etc.) are included directly in the `config.yaml`. Data about past members are instead organized in the folder `data/team` and are rendered through the markdown files in the folder `content/pastmembers`. *An important thing to keep in mind*: each of these markdown files retrieve the respective data through the parameter `team_year`, that should contain the exact name of the related file in the `data/team` folder.

### Update OHBM Brainhack website 

This is done through updating the hackathon repository.
Please see the instruction [here](https://github.com/ohbm/hackathon).


## Deploying
The OS-SIG website is currently hosted on [netlify](https://www.netlify.com/) under the account of Camille Maumet. 

Note: We have disabled the auto-publish option that automatically publishes online the updated website each time a new commit is pushed to the `master` branch. We did this because, for some unknown reasons, the deploys sometimes fails to properly create all the secondary pages (more specifically: there is no error but when clicking on the "Hackathon" link the page never loads). We have noticed that by re-running the deploy manually (sometimes more than once) the problem eventually disappears. With the auto-publish disabled, we can manually check that the latest deploys worked fine before manually publishing. 

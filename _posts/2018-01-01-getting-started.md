---
layout: post
title: "Getting Started"
author: "Sangeet Moy Das"
categories: journal
tags: [documentation,sample]
image: forest.jpg
---

# Sangeet.ai's Blog

Sangeet.ai's Blog uses a a minimalist Jekyll theme for running a personal blog or site for free through [Github Pages](https://pages.github.com/), or on your own server. Everything that you will ever need to know about this Jekyll theme is included in the README below, which you can also find in [the demo site](https://sangeetm.github.io/).

## Notable features

* Compatible with GitHub Pages.

* Support for Jekyll's built-in Sass/SCSS preprocessor and data files for making customizing easier.

* [Google Analytics](https://www.google.com/analytics/) support.

* Commenting support powered by [Disqus](https://disqus.com/).

* Optimized for search engines.

* LaTeX support through [MathJax](https://www.mathjax.org/).

## Table of Contents

1. [Introduction](#introduction)
   1. [What is Jekyll](#what-is-jekyll)
   2. [Never Used Jeykll Before?](#never-used-jekyll-before)
2. [Installation](#installation)
   1. [GitHub Pages Installation](#github-pages-installation)
   2. [Local Installation](#local-installation)
   3. [Directory Structure](#directory-structure)
   4. [Starting From Scratch](#starting-from-scratch)
3. [Configuration](#configuration)
   1. [Sample Posts](#sample-posts)
   2. [Site Variables](#site-variables)
   3. [Adding Menu Pages](#adding-menu-pages)
   4. [Posts](#posts)
   5. [Layouts](#layouts)
   6. [YAML Front Block Matter](#yaml-front-block-matter)
4. [Features](#features)
   1. [Design Considerations](#design-considerations)
   2. [Disqus](#disqus)
   3. [Google Analytics](#google-analytics)
   4. [RSS Feeds](#rss-feeds)
   5. [Social Media Icons](#social-media-icons)
   6. [MathJax](#mathjax)
   7. [Syntax Highlighting](#syntax-highlighting)
   8. [Markdown](#markdown)
5. [Everything Else](#everything-else)
6. [Contributing](#Contributing)
7. [Questions?](#questions)
8. [Credits](#credits)
9. [License](#license)

## Introduction

Sangeet.ai's Blog uses a Jekyll theme that was built to be 100% compatible with [GitHub Pages](https://pages.github.com/). If you are unfamiliar with GitHub Pages, you can check out [their documentation](https://help.github.com/categories/github-pages-basics/) for more information. [Jonathan McGlone's guide](http://jmcglone.com/guides/github-pages/) on creating and hosting a personal site on GitHub is also a good resource.

### What is Jekyll?

Jekyll is a simple, blog-aware, static site generator for personal, project, or organization sites. Basically, Jekyll takes your page content along with template files and produces a complete website. For more information, visit the [official Jekyll site](https://jekyllrb.com/docs/home/) for their documentation. Codecademy also offers a great course on [how to deploy a Jekyll site](https://www.codecademy.com/learn/deploy-a-website) for complete beginners.

### Never Used Jekyll Before?

The beauty of hosting your website on GitHub is that you don't have to actually have Jekyll installed on your computer. Everything can be done through the GitHub code editor, with minimal knowledge of how to use Jekyll or the command line. All you have to do is add your posts to the `_posts` directory and edit the `_config.yml` file to change the site settings. With some rudimentary knowledge of HTML and CSS, you can even modify the site to your liking. This can all be done through the GitHub code editor, which acts like a content management system (CMS).

## Installation

### GitHub Pages Installation

To start using Jekyll right away with GitHub Pages, [fork the repository on GitHub](https://github.com/SangeetM/sangeetm.github.io/fork). From there, you can rename your repository to 'USERNAME.github.io', where 'USERNAME' is your GitHub username, and edit the `settings.yml` file in the `_data` folder to your liking. Ensure that you have a branch named `gh-pages`. Your website should be ready immediately at 'http://USERNAME.github.io'. Note: if you are hosting several sites under the same GitHub username, then you will have to use [Project Pages instead of User Pages](https://help.github.com/articles/user-organization-and-project-pages/) - just change the repository name to something other than 'http://USERNAME.github.io'.

Head over to the `_posts` directory to view all the posts that are currently on the website, and to see examples of what post files generally look like. You can simply just duplicate the template post and start adding your own content.

### Directory Structure

If you are familiar with Jekyll, then the Blog directory structure shouldn't be too difficult to navigate. The following some highlights of the differences you might notice between the default directory structure. More information on what these folders and files do can be found in the [Jekyll documentation site](https://jekyllrb.com/docs/structure/).

```bash
sangeetm.github.io/
├── _data                      # Data files
|  └── settings.yml            # Theme settings and custom text
├── _includes                  # Theme includes
├── _layouts                   # Theme layouts (see below for details)
├── _posts                     # Where all your posts will go
├── assets                     # Style sheets and images are found here
|  ├── css                     # Style sheets go here
|  |  └── main.css             # Main CSS file
|  |  └── syntax.css           # Style sheet for code syntax highlighting
|  └── img                     # Images go here
├── menu                       # Menu pages
├── _config.yml                # Site build settings
├── Gemfile                    # Ruby Gemfile for managing Jekyll plugins
├── index.md                   # Home page
├── LICENSE.md                 # License for this theme
├── README.md                  # Includes all of the documentation for this theme
```

### Starting From Scratch

To completely start from scratch, simply delete all the files in the `_posts`, `assets/img`, and `menu` folder, and add your own content. You may also replace the `README.md` file with your own README. Everything in the `_data` folder and `_config.yml` file can be edited to suit your needs. You may also change the `favicon.ico` file to your own favicon.

## Configuration

### Sample Posts

Visit the [Sangeet.ai's Blog](https://sangeetm.github.io/) to find sample posts that show what different types of text formatting look like. You can find these posts in the `_posts` folder, which show what the best practices for setting up your own site are.

### Site Variables

To change site build settings, edit the `_config.yml` file found in the root of your repository, which you can tweak however you like. More information on configuration settings and plugins can be found on [the Jekyll documentation site](https://jekyllrb.com/docs/configuration/). This is also where you will be able to customize the title, description, and the author/owner of your site.

If you are hosting your site on GitHub Pages, then committing a change to the `_config.yml` file will force a rebuild of your site with Jekyll. Any changes made should be viewable soon after. If you are hosting your site locally, then you must run `jekyll serve` again for the changes to take place.

In the `settings.yml` file found in the `_data` folder, you will be able to customize your site settings, such as setting Disqus comments, Google Analytics, what shows up in your menu, and social media information.

### Adding Menu Pages

The menu pages are found in the `menu` folder in the root directory, and can be added to your menu in the `settings.yml` file.

### Posts

You will find example posts in your `_posts` directory. Go ahead and edit any post and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention of `YYYY-MM-DD-name-of-post.md` and includes the necessary front matter. Take a look at any sample post to get an idea about how it works.

### Layouts

There are two main layout options that are included with Sangeet.ai's Blog: post and page. Layouts are specified through the [YAML front block matter](https://jekyllrb.com/docs/frontmatter/). Any file that contains a YAML front block matter will be processed by Jekyll. For example:

```
---
layout: post
title: "Example Post"
---
```

Examples of what posts looks like can be found in the `_posts` directory, which includes this post you are reading right now. Posts are the basic blog post layout, which includes a header image, post content, author name, date published, social media sharing links, and related posts.

Pages are essentially the post layout without any of the extra features of the posts layout. An example of what pages look like can be found at the [About](https://sangeetm.github.io/menu/about.html) and [Contacts](https://sangeetm.github.io/menu/contact.html).

In addition to the two main layout options above, there are also custom layouts that have been created for the [home page](https://sangeetm.github.io/) and the [archives page](https://sangeetm.github.io/menu/writing.html). These are simply just page layouts with some [Liquid template code](https://shopify.github.io/liquid/). Check out the `index.html` file in the root directory for what the code looks like.

### YAML Front Block Matter

The recommended YAML front block is:

```
---
layout:
title:
author:
categories:
tags: []
image:
---
```

`layout` specifies which layout to use, `title` is the page or post title, `categories` can be used to better organize your posts, `tags` are used when generating related posts based on the topic of the post, and `image` specifies which images to use. Have a look at some posts in the `_posts` directory to see how these variables are set.

## Features

### Social Media Icons

All social media icons are courtesy of [Font Awesome](http://fontawesome.io/). You can change which icons appear, as well as the account that they link to, in the `settings.yml` file in the `_data` folder.

### MathJax

The Blog comes out of the box with [MathJax](https://www.mathjax.org/), which allows you to display mathematical equations in your posts through the use of [LaTeX](http://www.andy-roberts.net/writing/latex/mathematics_1).

### Syntax Highlighting

The Blog provides syntax highlighting through [fenced code blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks/). Syntax highlighting allows you to display source code in different colors and fonts depending on what programming language is being displayed. You can find the full list of supported programming languages [here](https://github.com/jneen/rouge/wiki/List-of-supported-languages-and-lexers). Another option is to embed your code through [Gist](https://en.support.wordpress.com/gist/).

### Markdown

As always, Jekyll offers support for GitHub Flavored Markdown, which allows you to format your posts using the [Markdown syntax](https://guides.github.com/features/mastering-markdown/). Examples of these text formatting features can be seen below. You can find this post in the `_posts` directory as well as the `README.md` file.

## Everything Else

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll's GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: http://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/

## Contributing

If you would like to make a feature request, or report a bug or typo in the documentation, then please [submit a GitHub issue](https://github.com/SangeetM/issues/new). If you would like to make a contribution, then feel free to [submit a pull request](https://help.github.com/articles/about-pull-requests/) - as a bonus, I will credit all contributors below! If this is your first pull request, it may be helpful to read up on the [GitHub Flow](https://guides.github.com/introduction/flow/) first.

## License

Open sourced under the [MIT license](https://github.com/SangeetM/LICENSE.md).

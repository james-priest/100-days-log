# 100 Days Log

This repo is used to track progress for Alexander Kallaway's 100 Days of Code Challenge ([https://100daysofcode.com](https://100daysofcode.com)).

It's available to anyone that would also like to track their progress using GitHub Pages. It uses a customized version of the [Leap day theme](https://github.com/pages-themes/leap-day) ([preview](https://pages-themes.github.io/leap-day/)) and allows simple customization of page titles & colors schemes.

## Overview

GitHub Pages is a static site hosting service provided by GitHub that takes Markdown files, combines them with a template, and turns them to static HTML.

With GitHub Pages enabled, code logs written in Markdown are converted to html when pushed to GitHib.

## Getting Started

GitHub Pages uses [Jekyll](https://jekyllrb.com/) to build the static site. Jekyll is a Ruby-based static site generator that uses [Liquid](https://jekyllrb.com/docs/liquid/) as it's templating language and Markdown as it's content source. Code logs are written in Markdown.

In order to preview and test changes, Jekyll GitHub Pages  should be installed locally. GitHub recommends installing Jekyll to preview your site and help troubleshoot any failed Jekyll builds.

While Jekyll relies on Ruby and Liquid for logic and templating, you don't need to know anything other than Markdown in order to create your log. Here are a couple Markdown resources.

- [GitHub Guides Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
- [Markdown Syntax Cheatsheet](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)

### Prerequisites

[Ruby](https://www.ruby-lang.org/) and [Bundler](http://bundler.io/) need to be installed before proceeding.

1. Open the terminal (Terminal, Git Bash, WSL, etc.).
2. Check whether you have Ruby 2.1.0 or higher installed:

   ```bash
   $ruby --version
   > ruby 2.X.X
   ```

3. If you don't have Ruby installed, [install Ruby 2.1.0 or higher](https://www.ruby-lang.org/en/downloads/).
4. Install Bundler:

   ```bash
   $ gem install bundler
   # Installs the Bundler gem
   ```

### Installation

Fork and clone the repo, then use Bundler to install the gem dependencies.

1. Fork the repo by clicking the Fork button in the upper right corner of the page.

    ![Fork button](./docs/src/fixed/fork.jpg)

2. Clone (or download) the repo.

    ```bash
    $ git clone https://github.com/<username>/100-days-log.git
    $ cd 100-days-log/docs/
    >
    ```

3. Install Jekyll and other [dependencies](https://pages.github.com/versions/) from the GitHub Pages gem with the following command.

    ```bash
    $ bundle install
    > Fetching gem metadata from https://rubygems.org/............
    > Fetching version metadata from https://rubygems.org/...
    > Fetching dependency metadata from https://rubygems.org/..
    > Resolving dependencies...

## Usage
You can serve the site and enable live-reload if desired. [Additional command line options](https://jekyllrb.com/docs/configuration/options/) exist to changes things such as port, hostname, url, etc.

### Serve site

Serves the local Jekyll site and rebuilds anytime a source file changes.

1. Navigate to the `docs` folder off of the root directory.
2. Run the Jekyll site locally.

    ```bash
    bundle exec jekyll serve
    ```

3. Preview your local Jekyll site in your web browser at

     [http://localhost:4000](http://localhost:4000)

### Serve site (with with live-reload)

Serves, builds and auto-reloads the page when whenever a source file changes.

1. Navigate to the `docs` folder off of the root directory.
2. Run the Jekyll site locally.

    ```bash
    bundle exec jekyll serve --livereload
    ```

3. Preview your local Jekyll site in your web browser at

     [http://localhost:4000](http://localhost:4000)

## Additional Automation Tasks

### Optimize images (jpg & png)

A grunt task is provided that will monitor a watch folder and create a small and large optimized version of any jpg or png files copied to that folder.

The small image is sized to display properly within the template's page width. The large image is used as an expanded view if a user clicks on the small image. Both are optimized for size.

Here are the source and destination folders. Once the Grunt task in running, any image copied to source will be optimized and place in output.

| Source folder | Output folder |
| --- | --- |
| `/docs/src/images/` | `/docs/assets/images/` |

The files are will be sized at

- small (570 width)
- large (800 width)

For example, an image named `my-file.jpg` will be created as follows.

| source | small output (570w) | large output (800w) |
| --- | --- | --- |
| /docs/src/images/my-file.jpg | /docs/assets/images/my-file_small.jpg | /docs/assets/images/my-file.jpg |

The images can then be linked to in the output directory from the code log.

#### Grunt Install

Run once to install package dependencies.

1. Navigate to the `docs` folder off of the root directory.
2. Install npm dependencies

    ```bash
    npm install
    ```

#### Grunt Usage

Run each time to enable image optimization with watch folder.

1. Navigate to the `docs` folder off of the root directory.
2. Run grunt task

    ```bash
    npx grunt
    ```

#### Embedding Images in Log

Use this format to embed a **simple, non-clickable** image.

```bash
![image alt text](assets/images/my-file_small.jpg)
```

Use this format to embed a **clickable image** which displays a larger version on click.

```bash
[![image alt text](assets/images/my-file_small.jpg)](assets/images/my-file.jpg)
```

## Customization

THIS SECTION IS A WIP...

### Update Log

Log files exist in the `/docs` folder. Here's how a sample set of files would be converted.

- README.md -> index.html
- log1.md -> log1.html
- log2.md -> log2.html
- notes.md -> notes.html

### Deploy site

Once the log look fine then it can be deployed with a commit and push.

```bash
git add .
git commit -m "Day 1: Deploy new log"
git push
```

## Customize

Various things can be customized including:

- Header text
- Header description
- Header background color
- Page background color
- Link color
- Favicon
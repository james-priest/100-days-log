# 100 Days Log

This repo is used to track progress for Alexander Kallaway's 100 Days of Code Challenge ([https://100daysofcode.com](https://100daysofcode.com)).

It's available for use by anyone that would also like to track their progress by forking this repo and creating their own log.

It's hosted on GitHub Pages and uses a customized version of the Leap Day theme.

## Overview

GitHub Pages is a static site hosting service provided by GitHub that takes markdown files, combines them with a template, and converts them to static HTML.

With GitHub Pages enabled, code logs written in Markdown are converted to html when pushed to GitHib.

## Getting Started

GitHub Pages uses [Jekyll](https://jekyllrb.com/) to build the static site. Jekyll is a Ruby-based static site generator that uses [Liquid](https://jekyllrb.com/docs/liquid/) as it's templating language and Markdown as it's content source. Code logs are written in Markdown.

In order to preview and test changes locally, a version of the Jekyll GitHub Pages site should be installed locally.

GitHub recommends installing Jekyll to preview your site and help troubleshoot any failed Jekyll builds.

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

Fork and clone the repo then use Bundler to install the gem dependencies.

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

### Build site

To build your local Jekyll site.

1. Navigate to the `docs` folder off of the root directory.
2. Run the Jekyll site locally.

    ```bash
    bundle exec jekyll serve
    ```

3. Preview your local Jekyll site in your web browser at

     [http://localhost:4000](http://localhost:4000)

### Optimize images (jpgs)

A grunt task is provided that will monitor files copied to the `/docs/src/images/` folder and create two optimized versions which will output to `/docs/assets/images/`.

The files are will be a small (570 width) and medium (800 width) sized jpg. For example:

- source: `/docs/src/images/my-file.jpg`

becomes: 

- small: `/docs/assets/images/my-file_small.jpg`
- med: `/docs/assets/images/my-file.jpg`

#### Grunt Install

1. Navigate to the `docs` folder off of the root directory.
2. Install npm dependencies

    ```bash
    npm install
    ```

#### Grunt Usage

1. Run grunt task

    ```bash
    npx grunt
    ```

2. In order to display the small image while also making it clickable to display the larger image you can use this markdown syntax.

    ```bash
    [![small image](/docs/assets/images/my-file_small.jpg)](/docs/assets/images/my-file.jpg)
    ```

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
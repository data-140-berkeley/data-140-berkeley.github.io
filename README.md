# Data 140 Course Website

[![Deploy Jekyll site to Pages](https://github.com/data-140-berkeley/data-140-berkeley.github.io/actions/workflows/jekyll.yml/badge.svg)](https://github.com/data-140-berkeley/data-140-berkeley.github.io/actions/workflows/jekyll.yml) [![Run all page tests](https://github.com/data-140-berkeley/data-140-berkeley.github.io/actions/workflows/rspec.yml/badge.svg)](https://github.com/data-140-berkeley/data-140-berkeley.github.io/actions/workflows/rspec.yml)

## Installation

Prerequisites:

- You have everything that [Jekyll requires](https://jekyllrb.com/docs/installation/)
- You have installed [Bundler](https://bundler.io/): `gem install jekyll bundler`

After cloning this repository and navigating into the directory, run the following command to install dependencies
```
cd data-140-berkeley.github.io
bundle install
```

## Usage

To run the site locally, run:

```
bundle exec jekyll serve
```

## Deployment

This site is deployed via a [GitHub Action Workflow](.github/workflows/jekyll.yml). For more information see [GitHub Pages](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll).

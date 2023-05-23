# GitHub Pages Source Code

This repository contains the source code for [mirohaller.com](https://www.mirohaller.com).

This is based on a fork from [academicpages](https://github.com/academicpages/academicpages.github.io) whose license is [here](./LICENSE).

## Locations of key files/directories

- Basic config options: [\_config.yml](_config.yml)
- Top navigation bar config: [\_data/navigation.yml](_data/navigation.yml)
- Single pages: [\_pages/](_pages)
- Collections of pages are .md or .html files in:
  - [\_publications/](_publications)
  - [\_posts/](_posts)
  - [\_talks/](_talks)
- Footer: [\_includes/footer.html](_includes/footer.html)
- Static files (like PDFs): [/files/](files/)
- Profile image (can set in \_config.yml): [images/profile.png](images/profile.png)

## Run locally

Locally build and serve the website with the following commands (and update it automatically during changes):
```
bundle exec jekyll build --watch
bundle exec jekyll serve --watch --port 8000
````

## TODOs

- Update research statement
- Display distinctions
- Link presentations

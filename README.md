# Starred

[![CI](https://github.com/schaafjs/starred/workflows/CI/badge.svg)](https://github.com/schaafjs/starred/actions) [![This Repository uses a generated Social Preview from @pqt/social-preview](https://img.shields.io/badge/%E2%9C%93-Social%20Preview-blue)](https://github.com/pqt/social-preview)

## Install

```bash

$ pip install starred
$ starred --username schaafjs --sort > README.md
```

## Usage

```bash
$ starred --help

Usage: starred [OPTIONS]

    GitHub starred

    Create your own Awesome List using GitHub stars!

    example:     starred --username schaafjs --sort > README.md

Options:
    --username TEXT    GitHub username
    --token TEXT       GitHub token
    --sort             Sort by language
    --repository TEXT  Repository name
    --message TEXT     Commit message
    --ci TEXT          Display CI status badge.
    --version          Show the version and exit.
    --help             Show this message and exit.
```
> `--ci` expects input of the form `![workflow name](https://github.com/<OWNER>/<REPOSITORY>/workflows/<WORKFLOW_FILE_PATH>/badge.svg)`

## Demo

```bash
# automatically create the repository
$ export GITHUB_TOKEN=yourtoken
$ starred --username yourname --repository awesome-stars --sort
```

- [`maguowei/awesome-stars`](https://github.com/maguowei/awesome-stars)
- [update awesome-stars every day by GitHub Action](https://github.com/maguowei/awesome-stars/blob/master/.github/workflows/schedules.yml) the example with GitHub Action

## Notice
This repository is a fork of https://github.com/maguowei/starred with the optional feature to display the status of your CI instead of the [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome) badge in the ```README.md``` file.

## FAQ

1. Generate new token

   link: [Github Personal access tokens](https://github.com/settings/tokens)

2. Why do I need a token?

   -  For unauthenticated requests, the rate limit is 60 requests per
      hour.
      see [Github Api Rate
      Limiting](https://developer.github.com/v3/#rate-limiting)
   -  The token must be passed together when you want to automatically
      create the repository.

3. Install the master branch version

    ```bash
    $ pip install -e git+https://github.com/schaafjs/starred.git
    ```

# ChangeLog Test

[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)

## Commit Tool

* global
  * `sudo npm install -g commitizen`
  * `sudo npm install -g cz-conventional-changelog`
  * `echo '{ "path": "cz-conventional-changelog" }' > ~/.czrc`
* init commitizen
  * `commitizen init cz-conventional-changelog --save-dev --save-exact`

## ChangeLog

* `npm install -g conventional-changelog-cli`
* `conventional-changelog -p angular -i CHANGELOG.md -s -r 0`
  * `-s` same file
  * `-r` how many releases to be generated from the lateset
    * `0`: the whole changelog will be regenerated and the outfile will be overwritten
    * `1`: default value

## Pipeline

1. hack code
2. `git add` new files and modified files
3. commit by `git cz`
4. if it is first update of new version
   * modify to new version in `package.json`
5. `npm run matadata`
6. `git push`
7. if it is last update of current version
   * `git tag <current_version> && git push --tags`

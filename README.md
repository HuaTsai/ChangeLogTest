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

1. write code
2. `git add`
3. `git cz`
4. modify version
5. `conventional-changelog -p angular -i CHANGELOG.md -s`
6. add and commit `package.json` and `CHANGELOG.md`
7. tag
8. push

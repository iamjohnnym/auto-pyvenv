# auto-pyvenv ChangeLog

## 1.0.1 2018-11-17
* Setup a virtualenv on the global version of python in the event `.python-version` is missing
* Install the python binary of the version declared in `.python-verson` file in the event it exists but the binary isnt installed
    * upgrade `pip`
    * upgrade `setuptools` as a preemtive move to in case its too old for `py2venv`
    * install `py2venv` for `python 2.x` versions.
* Added `VERSION` file

## 1.0.0 2018-11-16
* Added `.envrc` with instructions to configure a virtualenv
* Added `.travis.yml` file to test direnv with pyenv on various versions of python.
* Added `LICENSE.md`
* Added `RELEASE_POLICY.md`
* Added `CHANGELOG.md`
* Added Github Specific Files
    * `.gitignore`
    * `CONTRIBUTING.md`
    * `ISSUE_TEMPLATE.md`
    * `PULL_REQUEST_TEMPLATE.md`

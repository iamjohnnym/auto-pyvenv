[![Build Status](https://travis-ci.com/iamjohnnym/auto-pyvenv.svg?branch=master)](https://travis-ci.com/iamjohnnym/auto-pyvenv)
# Auto Pyvenv
[![forthebadge](https://forthebadge.com/images/badges/uses-badges.svg)](https://forthebadge.com)
[![forthebadge](https://forthebadge.com/images/badges/60-percent-of-the-time-works-every-time.svg)](https://forthebadge.com)

**RELATED ARTICLE** :: https://iamjohnnym.com/2018/11/15/managing-python-with-pyenv-and-direnv.html

This project is meant to ease the process of managing python for given projects.  Leveraging `pyenv`, `virtualenv`, and `direnv`, users will automatically create and source a python virtualenv for their projects.

# Table of contents

- [Auto Pyvenv](#auto-pyvenv)
- [Table of contents](#table-of-contents)
- [Usage](#usage)
    - [Installation](#installation)
    - [Uninstallation](#uninstallation)
- [Authors](#authors)
    - [Contributing](#contributing)
- [License](#license)
- [Versioning](#versioning)

# Usage

[(Back to top)](#table-of-contents)

Ensure you have both [pyenv](https://github.com/pyenv/pyenv) and [direnv](https://direnv.net/) installed on your system.

## Installation

[(Back to top)](#table-of-contents)

Navigate to the root dir of a python project and copy down this projects `.envrc`.  Having the file in this dir will trigger `direnv` to prompt you to allow execution of that file.

```sh
$ wget https://raw.githubusercontent.com/iamjohnnym/auto-pyvenv/master/.envrc
direnv: error .envrc is blocked. Run `direnv allow` to approve its content.
$ direnv allow
direnv: loading .envrc
Installing virtualenv for Python 3.7.0
Activating Python 3.7.0 virtualenv
Virtualenv has been activated for Python 3.7.0
/Users/iamjohnnym/.personal/tutorials/pyenv-direnv/.venv/bin/python
direnv: export +VIRTUAL_ENV ~PATH
```

You can also specify what version of python you want to use with your project by creating a `.python-version` file.

```sh
$ pyenv local 3.6.1
$ cat .python-version
3.6.1
$ pyenv versions
  system
  2.7.15
  3.5.0
* 3.6.1 (set by /Users/iamjohnnym/.personal/auto-venv/.python-version)
  3.7.0
```

## Uninstallation

[(Back to top)](#table-of-contents)

```sh
$ rm .envrc
```

# Authors
[(Back to top)](#table-of-contents)

* **Johnny Martin** - *Initial work* - [iamjohnnym](https://github.com/iamjohnnym)

See also the list of [contributors](https://github.com/iamjohnnym/auto-pyvenv/contributors) who participated in this project.

## Contributing

[(Back to top)](#table-of-contents)

Your contributions are always welcome! Please have a look at the [contribution guidelines](.github/CONTRIBUTING.md) first.

# License

[(Back to top)](#table-of-contents)

Apache License, Version 2.0 2018 - [Johnny Martin](https://github.com/iamjohnnym/). Please have a look at the [LICENSE.md](LICENSE.md) for more details.

# Versioning
[(Back to top)](#table-of-contents)

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/iamjohnnym/auto-pyvenv/tags).

# Python library cookiecutter template

Use 'cookiecutter' with this template to generate a new Python terminal application.

## Install cookiecutter

Cookiecutter can be installed using pip or conda, or as follows using pipx,
which makes it easy to install Python packages containing command-line tools, by
silently managing virtualenvs for installed packages, without you having to
worry about it. Hence:

    # First install pipx
    python3 -m pip install --user pipx

    # Then use pipx to install cookiecutter
    pipx install cookiecutter

## Using this template

Then run cookiecutter on this template to generate a directory containing a new
Python terminal application.

    cookiecutter gh:tartley/cookiecutter-python-termapp

(or, instead of 'gh:...', reference this directory on the local filesystem)

Answer the resulting prompts, or just press 'enter' to accept the shown
default values.

## Develop your code.

In your newly directory, run `make' with no target to see a list of supported
tasks.


## TODO

Things I want to add to this template:

* An actual placeholder app, that runs.
* source in 'src'
* incorporate argparse to make adding args simple.
* Makefile
  * self documenting
  * virtualenv management (maybe using 'tests', below, as a driver)
    Check the colorama one for nice fixes to virtualenv management.
    Figure out this in simon's template, which appears to be an alternative
    to separate requirements and requirements-dev files:
  
          pip install -e '.[test]'
  
  * build a wheel
  * generate requirements.txt from setup config? Or is there a better way?
    (one is used when pip installing this project, to also grab dependencies.
    (the other is used... erm... when? Why are there two?)
* tests using pytest. Run python in warning mode.
* Use tox to run against different python versions
    make test runs against current python
    make tox runs against earliest/latest supported versions
* linting
* github actions to run lint/tests on pushes
* github actions to push to pypi on github release
    - integrate release candidates into this.

* Can we eliminate the duplication between the README, and the top level package
  docstring, (which is output by pydoc and '--help'). Perhaps README should be
  generated from the docstring at build/release time?

Expand setup.cfg, & reduce setup.py to a shim.
https://snarky.ca/what-the-heck-is-pyproject-toml/
UPDATE: I believe setup.py can now be removed completely
Consider the replacements for each 'setup.py X' target detailed here:
https://blog.ganssle.io/articles/2021/10/setup-py-deprecated.html#summary

Consider creating pyproject.toml. (But cookiecutter itself uses something else)
But this involves the extra work of making [Neo]Vim read it.
But perhaps I want to do that anyway for work?

Readme overhaul, using sections taken from Colorama / Cbeams.
Including readme-hacking, especially release checklist.
Donate link in README. Can I just make up an `item_name`? (ie use PROJNAME)

Differentiate between:
* python terminal application
* python library
* python GUI application (later)
* python web service (later)
Differences:
* terminal app has a __main__.py, and corresponding entry point in setup.py
* libraries should specify deps as loosely specified as possible, apps should pin.
Does this require different templates? Can templates inherit or compose?


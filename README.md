# Python library cookiecutter template

Use 'cookiecutter' with this template to generate a new Python terminal application.

## Install cookiecutter

Cookiecutter can be installed using pip or conda, or using pipx. Pipx makes it
easy to manage installed Python packages containing command-line tools, by
silently dealing with virtualenvs for them. eg:

    # First install pipx
    python3 -m pip install --user pipx

    # Then use pipx to install cookiecutter
    pipx install cookiecutter

## Use this template

Then run cookiecutter on this template to generate a directory containing a new
Python terminal application.

    cookiecutter gh:tartley/cookiecutter-python-termapp

(or, instead of 'gh:...', reference this directory on the local filesystem)

Answer the resulting prompts, or just press 'enter' to accept the shown
default values.

## Develop your code

In your newly generated directory, run `make' with no target to see a list of
supported tasks.

## TODO

Things I want to add to this template:

* An actual placeholder app, that runs.
* source in 'src'
  https://hynek.me/articles/testing-packaging/
  * requirements.txt to list dependencies (none?)
  * requirements-dev.txt to list "-e ." and pytest?
  * then install requirements-dev.txt and then can run the app?
  * see how builds using hatch & requirements.txt were added to colorama
* Makefile
  * self documenting
  * virtualenv management (maybe using 'tests', below, as a driver)
  * Incorporate the great Makefile virtualenv building/population from
    code/done/bash-history-dedupe
  * Are there nice fixes in Colorama's Makefile?
    Figure out this in simon's template, which appears to be an alternative
    to separate requirements and requirements-dev files:
  
          pip install -e '.[test]'
  
  * Review the template 'Makefile' to check what should be taken from
    this repo's Makefile, to put into it, or visa-versa
  * build a wheel
  * generate requirements.txt from setup config? Or is there a better way?
    (one is used when pip installing this project, to also grab dependencies.
    (the other is used... erm... when? Why are there two?)
* tests using pytest. Run python in warning mode.
* incorporate argparse to make adding args simple.
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
    - has a __main__.py, and corresponding entry point in pyproject.toml
    - specify pinned deps in requirements.txt
* python library
And later:
* python GUI application
* python web service
Differences:
* libraries should specify deps as loosely specified as possible, apps should pin.
Does this require different templates? Can templates inherit or compose?
Consider putting all resulting templates into a single repo,
and choosing which one to use with `--directory`:
https://cookiecutter.readthedocs.io/en/stable/advanced/directories.html

Compile the python:
https://blog.glyph.im/2022/04/you-should-compile-your-python-and-heres-why.html


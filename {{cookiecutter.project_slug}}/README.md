# {{cookiecutter.project_name}}

[![PyPI](https://img.shields.io/pypi/v/{{cookiecutter.project_slug}}.svg)](https://pypi.org/project/{{cookiecutter.project_slug}}/)

[![Build Status](https://github.com/{{cookiecutter.github_username}}/{{cookiecutter.project_slug}}/actions/workflows/test.yml/badge.svg)](https://github.com/{{cookiecutter.github_username}}/{{cookiecutter.project_slug}}/actions/workflows/test.yml)

[![MIT License](https://img.shields.io/badge/License-MIT-blue)](https://mit-license.org/)

[![Github for source code](https://img.shields.io/github/v/release/{{cookiecutter.github_username}}/{{cookiecutter.project_name}}?include_prereleases&label=Github)](https://github.com/{{cookiecutter.github_username}}/{{cookiecutter.project_slug}})

{{cookiecutter.description}}

## Installation

{{cookiecutter.project_name}} can be installed using pip or conda, or using
pipx. Pipx makes it easy to manage installed Python packages containing
command-line tools, by silently dealing with virtualenvs for them. eg:

```bash
# First install pipx
python3 -m pip install --user pipx

# Then use pipx to install {{cookiecutter.project_slug}}
pipx install {{cookiecutter.project_slug}}
```

## Usage

Run from a terminal, eg:

```bash
{{cookiecutter.project_slug}} [OPTIONS]
```

Pass `--help` for more details.

## Status and Known Problems

This project is an unsupported experiment, created for fun. See [the github Issues
page](https://github.com/{{cookiecutter.github_username}}/{{cookiecutter.project_slug}}/issues).

## Development & Contributions

If you wish to make a contribution, consider creating an issue on GitHub first,
to discuss the idea before you do a bunch of work which might not get merged.

If you find {{cookiecutter.project_name}} useful, please [![Donate with PayPal](https://www.paypalobjects.com/en_US/i/btn/btn_donate_SM.gif)](https://www.paypal.com/donate/?business=2MZ9D2GMLYCUJ&no_recurring=0&item_name=Please+send+what+you+think+is+appropriate+for+your+use+of+{{cookiecutter.project_slug}}.+Thank+you%21&currency_code=USD) to the author. Thank you!


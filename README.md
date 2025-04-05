# cookiecutter-python-project

> Cookiecutter template for a standard python project that is pre-configured with libraries and tools I like



- Use [XDG Base Directory](https://specifications.freedesktop.org/basedir-spec/latest/) locations for configuration, log, and state files
- Use `src/` layout
- The module exposes a command line executable

## Guidelines and Dependencies 

- Use `uv pip install` to install dependencies
- Use `ruff` for lint and code formatting tasks
- Use the `structlog` module for logging
- Use the `config` module for configuration file procesing
- Use `pydantic` for all dataclasses 
- Use `sqlalchemy` for all SQL interactions
- Use `sqlite3` for SQL data storage
- Use `mypy` for static code analysis

## Creating a Project Using This Template

- To create a new project using this template, execute this command in your shell:

    ``` bash
    uv run cookiecutter 
    ```
- Don't forget to create and activate a virtual environment
    ``` bash
    uv venv
    source .venv/bin/activate
    ```


## Project Layout

This project is organized as a python module using the `src/` layout.

``` bash
.
├── README.md
├── default.cfg
├── pyproject.toml
├── src
│   └── cookiecutter_python_project
│       ├── __init__.py
│       ├── __main__.py
│       └── logger.py
├── tests
└── uv.lock
```

## To Create An Executable That Can Be Installed Standalone


To install a local version of the executable with a 

``` bash
uv tool install cookiecutter_python_project
```

To run the program without permanently installing it:

``` bash
uv run cookiecutter_python_project
```

## About Cookiecutter
The `cookiecutter` command is a command-line utility that creates projects from templates.

- Run cookiecutter with the shell command `uv run cookiecutter`. 
- More information about cookiecutter is available the project home page: [https://pypi.org/project/cookiecutter/](https://pypi.org/project/cookiecutter/).

## Important Caveats

- The project is pinned to python 3.11.1 for compatibility with some libraries that haven't been updated in a while. Feel free to change this to another python release 

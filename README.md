# Cipher &middot; [![Inline docs](https://inch-ci.org/github/dwyl/hapi-auth-jwt2.svg?branch=master)](https://github.com/apexDev37/Cipher/blob/main/README.md) [![Python version](https://img.shields.io/badge/-v3.12+-grey?style=flat&logo=python&logoColor=yellow)](https://www.python.org/downloads/) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-blue.svg)](http://makeapullrequest.com) [![Activity](https://img.shields.io/badge/status-active-brightgreen)](https://github.com/apexDev37/Cipher/commits/main)

> Attempt to pair with an LLM to supercharge user account recovery protocols.

## Table of Contents

- [Introduction](#introduction)
- [Motivation](#motivation)
- [Installing / Getting Started](#installing--getting-started)
  - [Prerequisites](#prerequisites)
  - [Local Setup](#local-setup)

## Introduction

Cipher is a small, LLM-powered, application that aims to enhance user account recovery. This is achieved by integrating an LLM into the account recovery protocol and process. Cipher showcases a real-life scenario of abstracting/hiding sensitive data in a process closely coupled to a Large Language Model. This is achieved by delegating business logic concerns to the application and assigning generative-dependent responsibilities to the LLM.

### Motivation

This repository is primarily for learning and experimentation, with the aim of leveraging it in future AI-powered, production-grade applications. I've recently been delving into and learning web security, prompted by a critical system I'm working on. Hence the theme and name for this repo which allows me to wear and test my "security hat"🤠💥

## Installing / Getting Started

This is an overview of the minimal setup needed to get started.

### Prerequisites

- [Git]
- [Python]
- IDE, Code/Text editor ([PyCharm], [VScode], [Vim], etc)

### Local Setup

> The following commands were run on Ubuntu focal (20.04.6 LTS)

- **Clone repository**

```bash
    # cd your/desired/target/dir
    $ git clone git@github.com:apexDev37/Cipher.git cipher
    $ cd cipher
```

> This command clones the repository into a target directory on your local machine with the name `cipher/` and navigates into the repository's root directory.

Create a virtual environment with your preferred package manager to isolate Cipher's required dependencies. I'm using `virtualenvwrapper`. See more details on [virtual environments] and [virtualenv].

- **Create virtual environment**

```bash
    $ mkvirtualenv -p python3.12 cipher
```

> This will create and activate a managed virtual env called `cipher` using a Python `3.12.x` interpreter on your local machine. Note: If you are not using `virtualenvwrapper`, run the command to create your virtual environment from the project's root directory.

- **Install required packages**

```bash
    # We need `pip-sync` for the next command
    $ pip install -r <(cat requirements/pip.txt requirements/pip-tools.txt)
    # Install packages and sync your venv
    $ pip-sync requirements/*.txt
```

> First, install `pip` and `pip-tools` requirements to access additional package management utilities. Next, use `pip-sync` to install all project requirements and _synchronize_ our active virtual environment with pinned package versions.

> ⚠ Note, if you face an issue while installing requirements, particularly with `langflow`, run the following setup commands and rerun `pip-sync ...`.

```bash
    # Ensure you have Python dev headers
    $ sudo apt install python3.x-dev    # Replace with your py version
    # Install other required dependencies
    $ sudo apt install build-essential libssl-dev libffi-dev libxml2-dev libxslt1-dev zlib1g-dev

```

> This first installs Python development headers on your local machine. Next, other dependencies essential for compiling and building Python packages, especially those with C extensions are installed.


[//]: # "These are reference links used in the body of this note and get stripped out when the markdown processor does
its job. There is no need to format nicely because it shouldn't be seen.
Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax"

<!-- Introduction links -->

<!-- Installing / Getting Started links -->

[Git]: https://git-scm.com/
[Python]: https://www.python.org/
[PyCharm]: https://www.jetbrains.com/pycharm/
[VScode]: https://code.visualstudio.com/
[Vim]: https://www.vim.org/

<!-- Installing / Getting Started links -->

[virtual environments]: https://docs.python.org/3/tutorial/venv.html
[virtualenv]: https://pypi.org/project/virtualenvwrapper/

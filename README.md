# TheInternAssistant

This project was developped as a part of [Mistral AI Fine-tuning Hackathon](https://mistral.ai/news/2024-ft-hackathon/).
The Intern Assistant aims to streamline and enhance productivity during multi-person calls by automatically gathering information, summarizing key points, and performing necessary follow-up actions.


## Table of Contents

- [Introduction](#introduction)
- [Goal](#Goal)
- [Access the Online Streamlit App](#usage)
- [Contact](#contact)

## Introduction

In today's fast-paced business environment, effective communication and efficient follow-up actions are crucial for success. However, managing meetings, especially with multiple participants, can be challenging. Important points may get lost, action items might be forgotten, and valuable time is spent on manual note-taking and task assignment.

## Goal
The goal of "The Intern Assistant" is to streamline and enhance productivity during multi-person calls by automatically gathering information, summarizing key points, and performing necessary follow-up actions. This innovative assistant ensures that important details are accurately captured, documented, and integrated with productivity tools, taking actions such as assigning tasks, scheduling follow-ups, and sending email summaries. By eliminating the need for manual note-taking, The Intern Assistant improves the efficiency and effectiveness of team collaboration and task management.


## Usage
### Python environment

The python environment must be `python3.10` and it can be created using the following command :
`python -m venv .venv`
or
`python3.10 -m venv .venv`

Then to activate the virtual environment :
- on UNIX --> `source .venv/bin/activate`
- on Windows powershell --> `.\.venv\Scripts\activate`

## Git workflow

### pre-commit hooks


After running `poetry install`, run this command to set the pre-commit hook :
`pre-commit install`

It will install the following hooks :
- ruff for formatting and linting
- poetry-check to validate the structure of the pyproject.toml
- poetry-lock to lock the dependencies specified in pyproject.toml
- poetry-export to export the lock file to a requirements.txt format


### Workflow

We are following [trunk based development](https://trunkbaseddevelopment.com/) principles for this project, it is a software development methodology that promotes a streamlined and collaborative workflow.

#### Rebasing

Since the pre-commit hooks can create a new `poetry.lock` and `requirements.txt` file, rebasing your branch to the the updated main version can be a struggle.

To do so, after a `git rebase main`, when having conflict with poetry related files, we are doing :
- `git checkout --ours requirements.txt`
- `git checkout --ours poetry.lock`
- `git add requirements.txt poetry.lock`

Thus, we keep the `poetry.lock` and `requirements.txt` from the branch `main`.
NB: while doing a `merge` instead of a `rebase`, `--ours` should be replaced with `--theirs`

## Environment variables

In order to use the project, you must create a `.env` file under the root directory.
You can use the `.env-template` to know what are the environment variables to fill.

## Access the Online Streamlit App
Open your web browser and navigate to the URL https://garkavem-mistral-genies-hackathon-main-lipp61.streamlit.app/.

After providing your Mistral API key, you can use the interactive interface to configure evaluation parameters, generate test samples, and view analysis results.


## Contact

For questions, feedback, or suggestions, please contact as or open an issue on GitHub
-  [Pascal LIM](https://www.linkedin.com/in/pascallimlink/)
-  [Karina Ashurbekova](https://www.linkedin.com/in/karina-ashurbekova/)
-  [Siwar ABBES](https://www.linkedin.com/in/siwar-abbes/)
-  [Xinyu (Judy) LAI](https://www.linkedin.com/in/xinyu-lai-hec-paris/)

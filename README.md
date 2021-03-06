# project_create

Creates and setups dirs for open hardware projects.

Requirements:
* [gh](https://cli.github.com/)
* [python-gitlab](https://python-gitlab.readthedocs.io/en/stable/index.html)
* [kicad-init.sh](https://techoverflow.net/scripts/kicad-init.sh)

For github usage ```gh auth login``` must be ran first.

For gitlab usage ```/etc/python-gitlab.cfg``` or ```${HOME}/.python-gitlab.cfg``` must be configured and the env var PROJECT_REPO_TYPE must equal 'gitlab' and be exported (I.E. ```export PROJECT_REPO_TYPE='gitlab'```), this can be added to your ```.bashrc``` or equivilant file for the choice to be persistant.
Either ```PROJECT_DIR_BASE``` must be a defined env var of fully quilified path, or ```${HOME}/Projects``` must exit.

Basic POSIX shell script, simply run as:
'''project_create YOUR_PROJECT_NAME'''


ENV_VARS:
```
PROJECT_DIR_BASE="${PROJECT_DIR_BASE:-${HOME}/Projects}"
PROJECT_REPO_TYPE="${PROJECT_REPO_TYPE:-github}"
```

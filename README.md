# new-macbook

I just got a new macbook, and have had to install a bunch of 💩 in order to get the setup I like. Documenting what I did here!


# Applications to Install

- Google Chrome
	- Some nice developer chrome extensions:
		- https://vimium.github.io/
		- https://chrome.google.com/webstore/detail/octotree/bkhaagjahfmjljalopjnoealnfndnagc
- iTerm2
- Spotify
- Slack
- R
    - http://cran.utstat.utoronto.ca/
    - R studio: https://www.rstudio.com/
    - R packages
        - ggplot2
        - data.table
        - dtplyr
        - dplyr
        - scales
        - zoo
        - RColorBrewer
        - plyr
        - RPostgreSQL
        - extrafont
        - lubridate
        - gridExtra
- Flux
- Divvy: http://mizage.com/divvy/
	- Used for replicating the only thing I liked about Windows: the cmd + arrow functionality to snap applications to the left/right of the screen, or to make them full screen
- Postico: https://eggerapps.at/postico/
- LICEcap: https://www.cockos.com/licecap/
    - screen recording software
- Google Drive: https://www.google.com/drive/download/

# Random things to install

- Homebrew: https://brew.sh/
- Oh-my-zsh: https://github.com/robbyrussell/oh-my-zsh
- Conda: https://conda.io/miniconda.html
- git: `brew install git`
- Update your `~/.gitconfig`

```
# This is Git's per-user configuration file.
[user]
        name = ian-whitestone
        email = XXX@gmail.com
```
- Generate a new github ssh key: https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/

- Postgres: [Instructions](https://www.codementor.io/engineerapart/getting-started-with-postgresql-on-mac-osx-are8jcopb)
    - `brew install postgresql`
    - `pg_ctl -D /usr/local/var/postgres start && brew services start postgresql`

- Jupyter Lab
    - Do the following in your base environment:
        - `conda install jupyter -y`
        - `conda install -c conda-forge jupyterlab -y`
        - `conda install nb_conda -y`
    - Get an R kernel available in jupyter lab
        - Run the following from R in terminal, not RStudio!
        - `install.packages("devtools")`
        - `devtools::install_github("IRkernel/IRkernel")`
        - `IRkernel::installspec()`

- Terraform: https://www.terraform.io/intro/getting-started/install.html
    - Terraform ships as a binary. I saved it in my home directory
    - Added the following to my `~/.zshrc`: `export PATH=$HOME/:$PATH`

# Application Specific Setups

## iTerm2

- [Setup instructions here](https://gist.github.com/kevin-smets/8568070) for oh-my-zsh, powerline font, etc.
- Profiles setup
    - Preferences -> Profiles -> Default -> Colors -> Select "solarized light" from *Color Presents..*

## VSCode
* Install `code` shell command, instructions [here](https://code.visualstudio.com/docs/setup/mac#_launching-from-the-command-line)

`settings.json`

```
{
    "workbench.colorTheme": "Solarized Light",
    "python.jediEnabled": false,
    "window.zoomLevel": 0,
    "data.preview.theme": "light",
    "terminal.integrated.fontFamily": "MesloLGS NF",
    "editor.minimap.enabled": false,
    "eslint.alwaysShowStatus": true,
    "eslint.format.enable": true,
    "eslint.codeAction.disableRuleComment": {},
    "editor.codeActionsOnSave": {
        "source.fixAll.eslint": true,
        "source.fixAll": true
    },
    "editor.formatOnSave": true,
    "eslint.run": "onSave",
    "python.languageServer": "Microsoft",
    "python.linting.flake8Enabled": true,
    "files.trimTrailingWhitespace": true,
    "python.linting.flake8Args": [
        "--config=.flake8"
    ],
    "[python]": {
        "editor.codeActionsOnSave": {
            "source.organizeImports": true
        }
    },
    "autoDocstring.customTemplatePath": "/Users/ianwhitestone/google_no_types.mustache",
    "python.linting.mypyEnabled": true,
    "python.formatting.provider": "black",
    "python.sortImports.path": "/Users/ianwhitestone/Library/Caches/pypoetry/virtualenvs/domi-IWOYYLRr-py3.7/bin/isort",
    "python.sortImports.args": [
        "-rc",
    ],
    "python.analysis.disabled": [
        "inherit-non-class"
    ],
}
```

# Other things to Setup

- iCloud
- vimrc: https://github.com/amix/vimrc

# Python

For some reason, Mac OS still ships with Python 2.7 (as of March 7, 2020). So install Python 3:

`brew install python3`

## pyenv

[pyenv](https://github.com/pyenv/pyenv) pyenv lets you easily switch between multiple versions of Python. Install it with brew:

`brew install pyenv`

Validate the installation worked:

```bash
→ pyenv --version
pyenv 1.2.16
```

Now install Python 3.7.6, and set it so that it is the global Python.

```bash
pyenv install 3.7.6
pyenv global 3.7.6
```

Validate that worked properly by running:

```bash
→ python --version
Python 3.7.6

→ which python
/Users/ianwhitestone/.pyenv/shims/python
```


**Poetry**

Install poetry with:

`curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python`

Then add `source $HOME/.poetry/env` to your `~/.zshrc` or `~/.bash_profile`, and then re-source your shell with `source ~/.zshrc` or `source ~/.bash_profile`.

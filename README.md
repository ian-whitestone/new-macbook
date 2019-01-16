# new-macbook

I just got a new macbook, and have had to install a bunch of 💩 in order to get the setup I like. Documenting what I did here!


# Applications to Install

- Google Chrome
	- Some nice developer chrome extensions:
		- https://vimium.github.io/
		- https://chrome.google.com/webstore/detail/octotree/bkhaagjahfmjljalopjnoealnfndnagc
- iTerm2
- SublimeText
- Spotify
- Slack
- R: http://cran.utstat.utoronto.ca/
- R studio: https://www.rstudio.com/
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
- Redis: https://medium.com/@petehouston/install-and-config-redis-on-mac-os-x-via-homebrew-eb8df9a4f298
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

# Application Specific Setups

## iTerm2

- Download cobalt theme: https://github.com/wesbos/Cobalt2-iterm
- Setup natural text editing mode: https://apple.stackexchange.com/questions/136928/using-alt-cmd-right-left-arrow-in-iterm
- Add the following to have your command prompt on a newline: `PROMPT="$PROMPT"$'\n'"%{$terminfo[bold]$fg[red]%}→ %{$reset_color%}"`
- Enable scrolling in vim: 
    - add `set mouse=a` to `~/.vimrc` (create it if it doesn't exist)
    - https://superuser.com/questions/238362/enable-mouse-for-scrolling-only-in-vim-in-iterm-macosx

## Sublime Text 3
- Launch sublime from terminal, and be able to open files/folders in sublime with `$ sublime my_file.txt`: https://ashleynolan.co.uk/blog/launching-sublime-from-the-terminal
- Install package control: https://packagecontrol.io/installation
- Sublime text packages:
    - Autodocstring: https://packagecontrol.io/packages/AutoDocstring
    - Cobalt2: https://github.com/wesbos/cobalt2
    - Pylint:
        - First install `SublimeLinter`, then `SublimeLinter-pylint`
        - Make sure you have pylint installed globally (`conda install pylint`)
        - Run `which pylint` to get the path, here's my output `/Users/ianwhitestone/miniconda3/bin/pylint`
        - see `sublime-linter-user-settings.json` for my settings
    - GitGutter
        - Added `"show_line_annotation": false` in user settings
    - [Whitespace](https://github.com/randy3k/Whitespace): trim trailing whitespace

- see `sublime-user-settings.json` for my Sublime Text User Settings


# Other things to Setup

- iCloud
- vimrc: https://github.com/amix/vimrc


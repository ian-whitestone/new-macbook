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
- Flux
- SizeUp: http://www.irradiatedsoftware.com/sizeup/
	- Used for replicating the only thing I liked about Windows: the cmd + arrow functionality to snap applications to the left/right of the screen, or to make them full screen
- Postico: https://eggerapps.at/postico/
	

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

# Application Specific Setups

## iTerm2

- Download cobalt theme: https://github.com/wesbos/Cobalt2-iterm
- Setup natural text editing mode: https://apple.stackexchange.com/questions/136928/using-alt-cmd-right-left-arrow-in-iterm
- Add the following to have your command prompt on a newline: `PROMPT="$PROMPT"$'\n'"%{$terminfo[bold]$fg[red]%}→ %{$reset_color%}"`

## Sublime Text 3
- Launch sublime from terminal, and be able to open files/folders in sublime with `$ sublime my_file.txt`: https://ashleynolan.co.uk/blog/launching-sublime-from-the-terminal
- Install package control: https://packagecontrol.io/installation
- Sublime text packages:
    - Autodocstring: https://packagecontrol.io/packages/AutoDocstring
    - Cobalt2: https://github.com/wesbos/cobalt2
    - Pylint

- Sublime Text User Settings

```json
{
    "bold_folder_labels": true,
    "caret_extra_bottom": 2,
    "caret_extra_top": 2,
    "caret_extra_width": 3,
    "caret_style": "phase",
    "color_scheme": "Packages/Theme - Cobalt2/cobalt2.tmTheme",
    "highlight_line": true,
    "highlight_modified_tabs": true,
    "ignored_packages":
    [
        "Vintage"
    ],
    "indent_guide_options":
    [
        "draw_normal",
        "draw_active"
    ],
    "line_padding_bottom": 1,
    "line_padding_top": 1,
    "theme": "Cobalt2.sublime-theme",
    "wide_caret": true,
    "translate_tabs_to_spaces": true,
    "rulers": [80]
}
```

# Other things to Setup

- iCloud
- vimrc: https://github.com/amix/vimrc


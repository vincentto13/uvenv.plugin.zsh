# uvenv.plugin.zsh
Plugin which extends regular oh-my-zsh! venv plugin functionality

## Installation
You're required to copy uvenv.plugin.zsh into your regular oh-my-zsh! plugin directory. Similar to example below

```
mkdir -p $ZSH/plugins/uvenv
cp uvenv.plugin.zsh $ZSH/plugins/uvenv
```

Enable plugin in your .zshrc file extending your regular list, for example
```
plugins=(git uvenv)
```

In case of any troubles please reffer to oh-my-zsh! documentation.

To have more benefit from using this plugin make sure you add virtualenv_prompt_info to the theme youre using, for example:

in regular $ZSH/themes/robbyrussell.zsh-theme file I've changed the following line

```
PROMPT='${ret_status} %{$fg[cyan]%}%c%{$reset_color%} $(git_prompt_info)'
```
into
```
PROMPT='${ret_status} %{$fg[cyan]%}%c%{$reset_color%} $(virtualenv_prompt_info) $(git_prompt_info)'
```

When you're done, the terminal would inform you about your virtualenv status, and give you some more commands.

```console
foo@bar:~$ whoami
foo
```

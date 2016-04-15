# Tmux Plugin Manager (for Termux)

[![Build Status](https://travis-ci.org/tmux-plugins/tpm.png?branch=master)](https://travis-ci.org/tmux-plugins/tpm)

Installs and loads TMUX plugins.

Tested and working on Android/Termux.

### Installation

Requirements: `tmux` version 1.9 (or higher), `git`, `bash`.

Clone TPM:

    $ git clone https://github.com/BenTGNU/tpm ~/.tmux/plugins/tpm

Put this at the bottom of `.tmux.conf`:

    # List of plugins
    set -g @plugin 'tmux-plugins/tpm'
    set -g @plugin 'tmux-plugins/tmux-sensible'

    # Other examples:
    # set -g @plugin 'github_username/plugin_name'
    # set -g @plugin 'git@github.com/user/plugin'
    # set -g @plugin 'git@bitbucket.com/user/plugin'

    # Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
    run '~/.tmux/plugins/tpm/tpm'

Reload TMUX environment so TPM is sourced:

    # type this in terminal
    $ tmux source ~/.tmux.conf

That's it!

### Installing plugins

1. Add new plugin to `~/.tmux.conf` with `set -g @plugin '...'`
2. Press `prefix + I` (capital I, as in **I**nstall) to fetch the plugin.

You're good to go! The plugin was cloned to `~/.tmux/plugins/` dir and sourced.

### Uninstalling plugins

1. Remove (or comment out) plugin from the list.
2. Press `prefix + alt + u` (lowercase u as in **u**ninstall) to remove the plugin.

All the plugins are installed to `~/.tmux/plugins/` so alternatively you can
find plugin directory there and remove it.

### Key bindings

`prefix + I`
- Installs new plugins from GitHub or any other git repository
- Refreshes TMUX environment

`prefix + U`
- updates plugin(s)

`prefix + alt + u`
- remove/uninstall plugins not on the plugin list

### More plugins

For more plugins, check [here](https://github.com/tmux-plugins).

### Docs

- [Help, tpm not working](docs/tpm_not_working.md) - problem solutions

More advanced features and instructions, regular users probably do not need
this:

- [How to create a plugin](docs/how_to_create_plugin.md). It's easy.
- [Managing plugins via the command line](docs/managing_plugins_via_cmd_line.md)
- [Changing plugins install dir](docs/changing_plugins_install_dir.md)
- [Automatic TPM installation on a new machine](docs/automatic_tpm_installation.md)

### Other goodies

- [tmux-sensible](https://github.com/tmux-plugins/tmux-sensible) - a set of 
  tmux options that should be acceptable to everyone
- [tmux-online-status](https://github.com/tmux-plugins/tmux-online-status) - a 
  plugin that enables displaying online status for your workstation
- [tmux-cpu](https://github.com/tmux-plugins/tmux-cpu) - enables displaying 
  cpu percentage and status icon in Tmux status-right
- [tmux-battery](https://github.com/tmux-plugins/tmux-battery) - enables 
  displaying battery percentage and status icon in tmux status-right

You might want to follow [@brunosutic](https://twitter.com/brunosutic) on
twitter if you want to hear about new tmux plugins or feature updates.

### License

[MIT](LICENSE.md)

# My VIM and TMUX Configuration

## VIM configuration

The vim configuration is based on the basic version of [this repo](https//github.com/amix/vimrc), to which 4 additional plugins are registered in the configuration file. We use [vim-plug](https://github.com/junegunn/vim-plug) as our plugin manager. 

### Install

To install, first copy `.vimrc` to your home folder, say `/home/username`. Second, copy `.vim/autoload/plug.vim` to your home folder, after which you should have something like  `/home/username/.vim/autoload/plug.vim`. Note the structure of the folder matters, since the plugin manager, which is needed to install other plugins, will not be loaded by vim. Last step is to install the plugins, in terminal, simply execute `vim +PlugInstall`.

### Plugins included

4 plugins are registered in the configuration file, they are:

- [ag.vim](https://github.com/rking/ag.vim.git): Search patterns in vim like ack. `ctrl+g` to trigger, type in the pattern and search.
- [LeaderF](https://github.com/Yggdroot/LeaderF.git): `;+f` to show filenames in quickfix buffer and fuzzy search files; `ctrl+b` to show opened files in quickfix buffer and fuzzy search; `ctrl+f` to show function signatures in the current file and fuzzy search.
- [onedark](https://github.com/joshdick/onedark.vim.git)
- [lightline](https://github.com/itchyny/lightline.vim.git) 

More details can be found on each plugin's github page.

To install plugins, find the block enclosed by `call plug#begin('~/.vim/plugged')` and `call plug#end()` and insert a line like `Plug 'URL_TO_YOUR_PLUGIN'` followed by `vim +PlugInstall` in the terminal or `:PlugInstall` in the normal mode when vim is open. 

To remove a plugin, simply comment out or remove the corresponding line in the block aforementioned. For detailed usage of the vim-plug, see their documentation.

### Useful shortcuts

Other useful shortcuts: to navigate between window splits, do `ctrl+arrow keys` or `ctrl+i/j/k/l`.

## TMUX configuration



To install, copy `.tmux.conf` to home folder. 

To create a named session, type `tmux new -s session_name` in terminal.

Once in a tmux session, `ctrl+b` to trigger commands.

Useful commands:

- `ctrl+b+s`: Split the current active window into two, horizontal edge of the two windows is shared.
- `ctrl+b+v`: Split the current active window into two, but share the vertical edge.
- `ctrl+b+i/j/k/l` or `ctrl+b+arrow keys` to navigate.
- `ctrl+b` and type `:a -t another_session` to attach to another session.
- `ctrl+b+d`: Detach the current session.

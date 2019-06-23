# Vundle
    vim bundle and plugin manager

## Source:
https://github.com/VundleVim/Vundle.vim

## Instructions:
1. Download Vundle

~~~
mkdir -p ~/.vim/bundle
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
~~~

2. [Configure Plugins](#https://github.com/VundleVim/Vundle.vim#quick-start "Click link and scroll to Step 3.")

~~~
vim .vimrc
~~~
Enter insert mode:
~~~
i
~~~
Paste the following at the top of the file:
~~~
set nocompatible              " be iMproved, required
filetype off                  " required

" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()
" alternatively, pass a path where Vundle should install plugins
"call vundle#begin('~/some/path/here')

" let Vundle manage Vundle, required
Plugin 'VundleVim/Vundle.vim'

" The following are examples of different formats supported.
" Keep Plugin commands between vundle#begin/end.
" plugin on GitHub repo
Plugin 'tpope/vim-fugitive'
" plugin from http://vim-scripts.org/vim/scripts.html
" Plugin 'L9'
" Git plugin not hosted on GitHub
Plugin 'git://git.wincent.com/command-t.git'
" git repos on your local machine (i.e. when working on your own plugin)
" Plugin 'file:///home/gmarik/path/to/plugin'
" The sparkup vim script is in a subdirectory of this repo called vim.
" Pass the path to set the runtimepath properly.
Plugin 'rstacruz/sparkup', {'rtp': 'vim/'}
" Install L9 and avoid a Naming conflict if you've already installed a
" different version somewhere else.
" Plugin 'ascenator/L9', {'name': 'newL9'}

" All of your Plugins must be added before the following line
call vundle#end()            " required
filetype plugin indent on    " required
" To ignore plugin indent changes, instead use:
"filetype plugin on
"
" Brief help
" :PluginList       - lists configured plugins
" :PluginInstall    - installs plugins; append `!` to update or just :PluginUpdate
" :PluginSearch foo - searches for foo; append `!` to refresh local cache
" :PluginClean      - confirms removal of unused plugins; append `!` to auto-approve removal
"
" see :h vundle for more details or wiki for FAQ
" Put your non-Plugin stuff after this line
~~~

3. Update

Enter normal mode in `.vimrc` by hitting the `Esc` key.

> Sometimes saving, exiting and re-entering `.vimrc` is required for the following cmd

Vundle can update itself when, within `.vimrc`, typing:
~~~
:PluginUpdate
~~~
Hit `q` to exit when done updating.


## Useful cmds:
|       cmd         |   description     |
|       ---         |       ---         |
| q                 | Exit view         |
| :PluginUpdate     | Update plugins    |
| :PluginInstall    | Install plugin    |
| :PluginList       | List plugins      |
| :PluginSearch     | Search plugins    |
| s                 | Search by name    |
| i                 | Install searched plugin  |


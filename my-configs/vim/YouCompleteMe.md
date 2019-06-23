# YouCompleteMe
	Autocomplete for vim.

## Source:
https://github.com/Valloric/YouCompleteMe

## Instructions:
> YCM is a plugin with a [compiled component](https://github.com/Valloric/YouCompleteMe#linux-64-bit). If you update YCM using Vundle and the ycm_core library APIs have changed (happens rarely), YCM will notify you to recompile it. You should then rerun the install process.

1. Install Vundle for vim

2. 

~~~
sudo apt update
sudo apt install -y build-essential cmake python3-dev
~~~

3. Enter `.vimrc`

~~~
vim ~/.vimrc
~~~
and type in the following:
~~~
Plugin 'https://github.com/Valloric/YouCompleteMe.git'
~~~
`vim-misc` is used by vim-notes to auto-load funcs.

4. Install the plugins:

> Sometimes saving, exiting and re-entering `.vimrc` is required for the following cmd

Enter the follwing, within `.vimrc`, in normal mode (can take ~10s to process):
~~~
:PluginInstall
~~~

5. Install completers

> If you need others completers, check the repo. You can also use the `./install.py` to install all supported languages.

~~~
cd ~/.vim/bundle/YouCompleteMe
python3 install.py --clang-completer
~~~
OR
~~~
python3 install.py
~~~

6. Additional autocomplete snippets:

Install these plugins

~~~
" Track the engine.
Plugin 'SirVer/ultisnips'
" Snippets are separated from the engine. Add this if you want them:
Plugin 'honza/vim-snippets'
" Trigger configuration. Do not use <tab> if you use https://github.com/Valloric/YouCompleteMe.
let g:UltiSnipsExpandTrigger="<tab>"
let g:UltiSnipsJumpForwardTrigger="<c-b>"
let g:UltiSnipsJumpBackwardTrigger="<c-z>"
" If you want :UltiSnipsEdit to split your window.
let g:UltiSnipsEditSplit="vertical"
~~~

## Errors during installation

In step 5.:
~~~
CMake Error: The source directory "~/.vim/bundle/YouCompleteMe/third_party/ycmd/third_party/cregex" does not appear to contain CMakeLists.txt.
Specify --help for usage, or press the help button on the CMake GUI.
ERROR: the build failed.
~~~

~~~
rm -rf ~/.vim/bundle/YouCompleteMe/third_party/ycmd/third_party/cregex
cd ~/.vim/bundle/YouCompleteMe/third_party && git submodule update --init --recursive 
~~~


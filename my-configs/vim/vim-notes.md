# vim-notes
	The only note taking this misses is embedding images and videos.

## Source:
https://github.com/xolox/vim-notes

## Instructions:
1. Install Vundle for vim

2. Enter `.vimrc`

~~~
vim ~/.vimrc
~~~
and type in the following:
~~~
Bundle 'https://github.com/xolox/vim-misc.git'
Bundle 'https://github.com/xolox/vim-notes.git'
~~~
`vim-misc` is used by vim-notes to auto-load funcs.

3. Install the plugins:

> Sometimes saving, exiting and re-entering `.vimrc` is required for the following cmd

Enter the follwing, within `.vimrc`, in normal mode:
~~~
:PluginInstall
~~~

## Usage
1. Enter vim
~~~
$ vim
~~~
2. Enter a file name
~~~
:Note Foo
~~~

## Where are notes saved?

In:

`~/.vim/bundle/vim-notes/misc/notes/user/`

## Useful cmds
|       cmd         |   description     |
|       ---         |       ---         |
| :Note             | Create note       |
| :SearchNotes     	| Search notes grep |
| gf	           	| on link => go to link |



# vim
Replicable vim configuration. All in one place and easy to acces.

### Install Plug  
```
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```
### Copy vimrc file 
```
"========================================================
"                  Plugin support
"========================================================
call plug#begin('~/.vim/plugs')
Plug 'https://github.com/sheerun/vim-polyglot.git'
Plug 'https://github.com/ParamagicDev/vim-medic_chalk.git'
call plug#end()
"Run plugInstall to install

"========================================================
"                    Tab Settings
"========================================================

function! UseTabs()
    set tabstop=4     " Size of a hard tabstop (ts).
    set shiftwidth=4  " Size of an indentation (sw).
    set noexpandtab   " Always uses tabs instead of space characters (noet).
    set autoindent    " Copy indent from current line when starting a new line (ai).
endfunction

function! UseSpaces()
  set tabstop=4     " Size of a hard tabstop (ts).
  set shiftwidth=4  " Size of an indentation (sw).
  set expandtab     " Always uses spaces instead of tab characters (et).
  set softtabstop=0 " Number of spaces a <Tab> counts for. When 0, featuer is off (sts).
  set autoindent    " Copy indent from current line when starting a new line.
  set smarttab      " Inserts blanks on a <Tab> key (as per sw, ts and sts).
endfunction
"use :retab to convert existing tabs into spaces
"
call UseSpaces()
set list
set listchars=tab:>-

"================================================================
"                           Cosmetics
"================================================================
set nu "line numbers
"set termguicolors "24-bit values for RGB colors
colorscheme medic_chalk 
"highlight LineNr ctermfg=white
```

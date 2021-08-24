# Nvim settings 

Custom neovim for frontend development

Settings:

```bash
set nocompatible
filetype off
syntax on
filetype plugin indent on
set modelines=0
set wrap
set formatoptions=tcqrn1
set tabstop=2
set shiftwidth=2
set softtabstop=2
set expandtab
set noshiftround
set backspace=indent,eol,start
set ttyfast
set showmode
set showcmd
set matchpairs+=<:>
set list
set listchars=tab:›\ ,trail:•,extends:#,nbsp:.
set encoding=utf-8
set hlsearch
set ignorecase
set smartcase
set nu rnu
set ruler
set termguicolors
```

Plugins:

```bash
call plug#begin(has('nvim') ? stdpath('data') . '/plugged' : '~/.vim/plugged')
Plug 'tpope/vim-sensible'
Plug 'junegunn/fzf', { 'do': { -> fzf#install() } }
Plug 'junegunn/fzf.vim'
Plug 'kyazdani42/nvim-web-devicons'
Plug 'kyazdani42/nvim-tree.lua'
Plug 'vim-airline/vim-airline'
Plug 'vim-airline/vim-airline-themes'
Plug 'mustache/vim-mustache-handlebars'
Plug 'mattn/emmet-vim'
Plug 'ghifarit53/tokyonight-vim'
Plug 'neoclide/coc.nvim' , { 'branch' : 'release' }
Plug 'caenrique/nvim-toggle-terminal'
Plug 'zefei/vim-wintabs'
Plug 'zefei/vim-wintabs-powerline'
Plug 'preservim/nerdcommenter'
Plug 'prettier/vim-prettier', {
  \ 'do': 'yarn install',
  \ 'for': ['javascript', 'typescript', 'css', 'less', 'scss', 'html'] }
call plug#end()
```

Handlebars fix

```bash
augroup handlebars_ft
  au!
  autocmd BufNewFile,BufRead *.hbs set filetype=handlebars
augroup END
```

set nocompatible              " required
filetype off                  " required

" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()

" alternatively, pass a path where Vundle should install plugins
" call vundle#begin('~/some/path/here')

" let Vundle manage Vundle, required
Plugin 'gmarik/Vundle.vim'

" Add all your plugins here (note older versions of Vundle used Bundle instead of Plugin)

" code folding
Plugin 'tmhedberg/SimpylFold'

" 自动补全
" Plugin 'Valloric/YouCompleteMe'

" Jedi - an awesome autocompletion/static analysis library for Python
"Plugin 'davidhalter/jedi'

" jedi-vim - awesome Python autocompletion with VIM
Plugin 'davidhalter/jedi-vim'

" PEP8自动缩进
Plugin 'vim-scripts/indentpython.vim'

" Python sytax checker/highlight
Plugin 'nvie/vim-flake8'
Plugin 'scrooloose/syntastic'

" Auto Comment 
Plugin 'scrooloose/nerdcommenter'

" Colors
Plugin 'jnurmine/Zenburn'
Plugin 'altercation/vim-colors-solarized'

" Auto Pairs
" Plugin 'jiangmiao/auto-pairs'

" Plugin on GitHub repo
" Supertab
" Plugin 'ervandew/supertab'

" filesystem
Plugin 'scrooloose/nerdtree'
" tab-key brower filetree
Plugin 'jistr/vim-nerdtree-tabs'

" find file in vim:ctrl+p
Plugin 'kien/ctrlp.vim'

" Powerline状态栏
Plugin 'Lokaltog/powerline', {'rtp': 'powerline/bindings/vim/'}

" markdown
Plugin 'plasticboy/vim-markdown'

" git in vim
Plugin 'tpope/vim-fugitive'

" A simple http/json wrapper around jedi.
" Plugin 'vheon/JediHTTP'

" All of your Plugins must be added before the following line
call vundle#end()            " required
filetype plugin indent on    " required

" 指定屏幕上可以进行分割布局的区域
set splitbelow
set splitright

" splite navigations
nnoremap <C-J> <C-W><C-J>
nnoremap <C-K> <C-W><C-K>
nnoremap <C-L> <C-W><C-L>
nnoremap <C-H> <C-W><C-H>

" Enable dolding
set foldmethod=indent
set foldlevel=99
" Enable  coding folding
nnoremap <space> za

" 看到折叠代码的文档字符串
let g:SimpyFold_docstring_preview=1

" 标示不必要的空白
au BufRead,BufNewFile *.py,*.pyw,*.c,*.h match BadWhitespace /\s\+$/


" 配色方案判断逻辑
if has('gui_running')
    set background=dark
    colorscheme solarized
else
	" Vbundle 找不到zenburn,来一句开机问候语
    colorscheme zenburn
	"echo  "Welcome, Merlin!"
endif

" Solarized方案同时提供了暗色调和轻色调两种主题。要支持切换主题功能(按F5)
call togglebg#map("<F5>")

" zenburn配色方案
set t_Co=256
" colors  zenburn

" display line number
set nu

" 自动补全
"let g:ycm_autoclose_preview_window_after_completion=1
"map <leader>g  :YcmCompleter GoToDefinitionElseDeclaration<CR>
let g:ycm_python_binary_path = '/usr/bin/python3'


" 文件浏览时隐藏.pyc文件
let NERDTreeIgnore=['\.pyc$', '\~$'] "ignore files in NERDTree

" Supertab
"let g:SuperTabDefaultCompletionType="<c-n>"
"let g:SuperTabDefaultCompletionType="context"
"let g:SuperTabContextDefaultCompletionType="<c-n>"

" no swap files
set noswapfile

"------------Start Web Page Stuff--------------------
au BufNewFile,BufRead *.js,*.html,*.css set tabstop=2
au BufNewFile,BufRead *.js,*.html,*.css set softtabstop=2
au BufNewFile,BufRead *.js,*.html,*.css set shiftwidth=2
au BufNewFile,BufRead *.js,*.html,*.css set expandtab

"------------Start Python PEP 8 stuff----------------
"" Number of spaces that a pre-existing tab is equal to.
au BufNewFile,BufRead *.py,*.pyw,*.c,*.h set tabstop=4

" spaces for indents
au BufNewFile,BufRead *.py set softtabstop=4
au BufNewFile,BufRead *.py,*.pyw set shiftwidth=4
au BufNewFile,BufRead *.py,*.pyw set expandtab

" Use the below highlight group when displaying bad whitespace is desired.
highlight BadWhitespace ctermbg=red guibg=red

" The maximum length of a line
au BufNewFile,BufRead *.py,*.pyw set textwidth=79

" Keep indentation level from previous line:
autocmd FileType python set autoindent
" Use UNIX (\n) line endings.
au BufNewFile *.py,*.pyw,*.c,*.h set fileformat=unix

" Set the default file encoding to UTF-8:
set encoding=utf-8

" For full syntax highlighting:
let python_highlight_all=1
syntax on

" Quick start NERDTree:F3
nmap <F3> :NERDTree <CR>

"<leader> 相当于一个前缀
let mapleader="\\"

" Start completions
let g:jedi#completions_command = "<C-Space>"

" Go to definition (or assignment) 
let g:jedi#goto_command = "<leader>d"

" Go to original definition
let g:jedi#goto_assignments_command = "<leader>g"

" Show pydoc documentation
let g:jedi#documentation_command = "K"

" Show usages of a name.
let g:jedi#usages_command = "<leader>n"

" Rename variables 
let g:jedi#rename_command = "<leader>r"

" Go to original definition
let g:jedi#goto_definitions_command = ""

" use tabs when going to a definition
"let g:jedi#use_tabs_not_buffers = 1

" no completion 
"let g:jedi#completions_enabled = 0

" 支持方向键和退格键
"set nocompatible
"set backspace=2

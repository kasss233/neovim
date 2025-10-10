call plug#begin('~/.config/nvim/plugged')

" 文件管理
Plug 'preservim/nerdtree'

" 补全 & LSP
Plug 'neoclide/coc.nvim', {'branch': 'release'}

" 自动括号
Plug 'jiangmiao/auto-pairs'

" 状态栏
Plug 'vim-airline/vim-airline'

" 快捷键提示
Plug 'folke/which-key.nvim'

Plug 'Chiel92/vim-autoformat'

call plug#end()
set number                  " 显示行号
syntax on                   " 开启语法高亮
set ignorecase smartcase    " 搜索大小写智能匹配
let mapleader="\<Space>"

nnoremap <leader>f :Autoformat<CR>
nnoremap <leader>q :q<CR>
nnoremap <leader>tt :term<CR>
nnoremap <leader>tn :tabnew<CR>
nnoremap <leader>th :tabprev<CR>
nnoremap <leader>tl :tabnext<CR>
nnoremap <leader>n :NERDTreeToggle<CR>
nnoremap <leader>d :CocDiagnostics<CR>
nnoremap <leader>h <C-w>h
nnoremap <leader>j <C-w>j 
nnoremap <leader>k <C-w>k
nnoremap <leader>l <C-w>l
tnoremap <Esc> <C-\><C-n>
" 使用 coc.nvim 提示时的 Tab 和 Enter 行为
inoremap <silent><expr> <TAB>
      \ coc#pum#visible() ? coc#pum#next(1) :
      \ CheckBackspace() ? "\<Tab>" :
      \ coc#refresh()

inoremap <silent><expr> <S-TAB>
      \ coc#pum#visible() ? coc#pum#prev(1) : "\<C-h>"

inoremap <silent><expr> <CR>
      \ coc#pum#visible() ? coc#pum#confirm() :
      \ "\<C-g>u\<CR>\<c-r>=coc#on_enter()\<CR>"

" 辅助函数：判断光标前是否有空格
function! CheckBackspace() abort
  let col = col('.') - 1
  return !col || getline('.')[col - 1]  =~ '\s'
endfunction


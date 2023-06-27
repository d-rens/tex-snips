# Notes on this fork

I have changed some things, disabled others...

The main change is that i am not using the 'math environment' variable, because i have not yet found a way to make it work with neovim instead of vim. 
Out of this i added letters to snippets to not use them accidentaly, it is a bit odd, but it works.

For example, `sr` was used to do `^2` but because `sr` is also used a lot in text i changed it to `srr`, similar with a lot of other snippets.

The quality of them decrese when doing that, so i am looking into making it work, it's probably possible.


# Vim + LaTeX snippets setup

*[How I'm able to take notes in mathematics lectures using LaTeX and Vim](https://castel.dev/post/lecture-notes-1/)*

## Vim configuration

Copy `tex.snippets` to `~/.vim/UltiSnips/` and assuming you're using [Vim Plug](https://github.com/junegunn/vim-plug), add the following to your `.vimrc`:

```vim
Plug 'sirver/ultisnips'
    let g:UltiSnipsExpandTrigger = '<tab>'
    let g:UltiSnipsJumpForwardTrigger = '<tab>'
    let g:UltiSnipsJumpBackwardTrigger = '<s-tab>'

Plug 'lervag/vimtex'
    let g:tex_flavor='latex'
    let g:vimtex_view_method='zathura'
    let g:vimtex_quickfix_mode=0

Plug 'KeitaNakamura/tex-conceal.vim'
    set conceallevel=1
    let g:tex_conceal='abdmg'
    hi Conceal ctermbg=none

setlocal spell
set spelllang=en_us
inoremap <C-l> <c-g>u<Esc>[s1z=`]a<c-g>u
```

For the colorscheme, install [pywal](https://github.com/dylanaraps/pywal), add the following to your `.vimrc`

```vim
Plug 'dylanaraps/wal'
colorscheme wal
set background=dark
```

Finally, execute `wal --theme base16-nord`.

Something not working as expected? Feel free to open an issue!

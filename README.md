# whitewriter [▎](https://github.com/mipmip/vim-whitewriter)

  Whitewriter is a fork of Typewriter but with a pure white background.

  A minimalistic vim and gvim colorscheme inspired by the great iA Writer editor.
  This repo contains the light (whitewriter.vim) and dark (whitewriter-dark.vim)
  versions.

  NOTE: whitewriter can only be used in terminals with true color support. E.g.
  [st](https://st.suckless.org/)

## Installation

  - You can use your vim plugin manager of choice
  - Or manually
    - Clone this repo.
    - Copy `colors/*.vim` to `~/.vim/colors/`


## Usage

  To enable this colorscheme, set in your .vimrc file:

  ```vim
    colorscheme whitewriter
    " or whitewriter-night
  ```

  You might need some extra configuration for true color support:

  ```vim
  set termguicolors
  let &t_8f = "\<Esc>[38;2;%lu;%lu;%lum"
  let &t_8b = "\<Esc>[48;2;%lu;%lu;%lum"
  ```

## Extras

  If you want a closer feel to iA Writer install

  - [goyo.vim](https://github.com/junegunn/goyo.vim) for focus mode.
  - [limelight.vim](https://github.com/junegunn/limelight.vim) for line
    highlight.

  and add this lines to vimrc:

  ```vim
    " Activate FOCUS mode with F12
    nmap <F12> :Goyo <bar> Limelight!!<CR>"


    " Change the cursor from block to i-beam in INSERT mode
    let &t_SI = "\e[5 q"
    let &t_EI = "\e[1 q"
    augroup myCmds
      au!
      autocmd VimEnter * silent !echo -ne "\e[1 q"
    augroup END
  ```

### Screenshots

![vim](https://logico.com.ar/img/2018/08/13/screenshot_a.png)

  ![gui vim](https://logico.com.ar/img/2018/08/13/screenshot_g.png)

  ![vim focus mode](https://logico.com.ar/img/2018/08/13/screenshot_b.png)

  ![fake bussy](https://logico.com.ar/img/2018/08/13/screenshot_c.png)

  ![whitewriter night vim](https://logico.com.ar/img/2018/08/13/screenshot_d.png)

  ![whitewriter night vim focus mode](https://logico.com.ar/img/2018/08/13/screenshot_e.png)

  ![whitewriter night gui vim](https://logico.com.ar/img/2018/08/13/screenshot_f.png)

  The font used in the screenshots is SF Mono 12 with letter space of -1 and
  line space of 8.

  ```
    # .Xresources file
    URxvt*letterSpace   : -1
    URxvt*lineSpace     : 8
  ```

  or if you use gVim o MacVim

  ```
    # .gvimrc file
    set linespace = 8
  ```

---

## Thanks

  Whitewriter is forked from [Typewriter](https://github.com/logico/typewriter-vim)

  Whitewriter is based/inspired by these projects

  - [iA Writer](https://ia.net/writer/)
  - [Vim colorschemes](https://github.com/flazz/vim-colorschemes)


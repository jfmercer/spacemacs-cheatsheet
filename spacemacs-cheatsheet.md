NOTE: "SPC and M-x can be used interchangeably".

Leader Key: `SPC`
Universal Argument: `SPC-u`
M-x: `:` == `SPC SPC`. That is, emacs's Meta-x (M-x) is `SPC SPC` which is identical to vim's `:`.

#### General Commands

* `C-/`: Undo
* `C-?`: Redo
* `SPC ?`: Search for keybindings


#### Configuration

* `f e d`: edit `.spacemacs` (files emacs dotfile)
* `f e R`: reload `.spacemacs` (files emacs Reload)
* `f e D`: diff `.spacemacs` with previous version (files emacs Diff)

#### Buffers

* `SPC b b`: helm-mini (buffers buffer)
* `SPC <tab>`: switch between open buffers
* `SPC b N`: create new, empty buffer (buffers New)
* `SPC b n/p`: next/previous buffer (buffers next/previous)
* `SPC b d`: delete current buffer (buffers delete)
* `SPC b .`: transient state buffer
* `SPC b m`: kill all buffers except current (buffers massacre)
* `SPC b C-d`: kill buffers matching a regex (buffers Controlled destruction)
* `SPC j l`: jump to any line in a buffer (jump line)
* `SPC s s`: search within buffer (search swoop)

#### Windows

Keybinding | Function
--- | ---
`SPC w v` OR `:vsplit` | Open vertical window on right (window vertical)
`SPC w s` OR `:split` | Open horizontal window below (window split)
`SPC w h/j/k/l` | Navigate among windows
`SPC w H/J/K/L` | Move the current window
`SPC w .` | Window transient state

#### Files

Keybinding | Function
--- | ---
`SPC f f` | Search files in current directory (files find)
`SPC f r` | Search recent files (files recent)
`SPC f s` OR `:w` | Save current file
`:x` | Save the current file and quit
`:e <file>` | Open `<file>`

#### Evil

* `fd`: `ESC`
* [evil-tutor](https://github.com/syl20bnr/evil-tutor): `SPC h T`
* `vim-surround`
    * Unlike the original `vim-surround`, `s` rather than `S` is used in visual mode
    * `cs"'`   : `"Hello world!"` --> `'Hello world!'`
    * `cs'<q>` : --> `<q>Hello world!</q>`
    * `cst"`   : --> `"Hello world!"`
    * `ds"`    : --> `Hello World!`
    * `ysiw`   : `Hello` --> `[Hello]`
    *  `cs]{`  : --> `{Hello}`
    * `yssb`   : `{Hello} world!` --> `({ Hello } world!)`
    * `yss)`   : same effect as `yssb`
    * `ds{ds)` : --> `Hello World!`
    * `ysiw<em>` : `Hello` --> `<em>Hello</em>`
    * For visual mode, `Vs<p class="important">` -->
    ```html
        <p class="important">
          <em>Hello</em> world!
        </p>
    ```

* Evil plugins

Spacemacs ships with the following evil plugins:

Mode | Description
-----| -----
[evil-args](https://github.com/wcsmith/evil-args) | motions and text objects for arguments
[evil-exchange](https://github.com/Dewdrops/evil-exchange) | port of [vim-exchange](https://github.com/tommcdo/vim-exchange)
[evil-indent-textobject](https://github.com/cofi/evil-indent-textobject) | add text object based on indentation level
[evil-matchit](https://github.com/redguardtoo/evil-matchit) | port of [matchit.vim](http://www.vim.org/scripts/script.php?script_id=39)
[NeoTree](https://github.com/jaypei/emacs-neotree) | mimic [NERD Tree](https://github.com/scrooloose/nerdtree)
[evil-nerd-commenter](https://github.com/redguardtoo/evil-nerd-commenter) | port of [nerdcommenter](https://github.com/scrooloose/nerdcommenter)
[evil-numbers](https://github.com/cofi/evil-numbers) | like `C-a` and `C-x` in vim
[evil-search-highlight-persist](https://github.com/juanjux/evil-search-highlight-persist) | emulation of hlsearch behavior
[evil-surround](https://github.com/timcharper/evil-surround) | port of [vim-surround](https://github.com/tpope/vim-surround)
[evil-visualstar](https://github.com/bling/evil-visualstar) | search for current selection with `*`

* vim motions: [avy](https://github.com/abo-abo/avy) enables jumping around text
* `SPC j j`: jump char
* `SPC j w`: jump word
* `SPC j l`: jump line

#### Helm

* `SPC SPC`: open helm
* `<tab>` completion is not supported. In fact, part of the whole idea in Helm is to provide something better than tab completion.
* `<tab>` or `C-i` lists available actions
* `C-j` or `C-z` invokes the persistent action
* `SPC w b`: refocus helm (window mini-buffer)

#### Shell

* `SPC '`: open shell in popup
* `SPC u SPC '`: open shell in current buffer
* `SPC p '`: open shell in project root
* `SPC m H`: browse history with `helm`
* `C-j`/`C-k`: next/previous item in history
* `{n} SPC '`: open n number of shells
* multi-term
    * `SPC m c`: create new multi-term
    * `SPC m n`: go to next multi-term
    * `SPC m p`: go to previous multi-term

#### Magit

#### Modeline

* Toggle Nyan Cat: `SPC t m n` (toggle modeline nyan)

#### Layers

* Open Layer: `SPC l o` (layer open)

#### Help

* General

    * `SPC h SPC`: spacemacs documentation
    * `SPC h m`: search man pages

* Describe functions

Key Binding | Description
--- | ---
`SPC h d b` | describe bindings in a `helm` buffer
`SPC h d c` | describe current character under point
`SPC h d d` | describe current expression under point
`SPC h d f` | describe a function
`SPC h d k` | describe a key
`SPC h d K` | describe a keymap
`SPC h d m` | describe a mode
`SPC h d p` | describe a package (emacs built-in function)
`SPC h d P` | describe a layer (Spacemacs)
`SPC h d v` | describe a variable

* `help-mode` navigation

Key Binding | Description
--- | ---
`g b` or `[` | go back
`g f` or `]` | go forward
`g h` | go to help for symbol under point

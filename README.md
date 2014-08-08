# vim-ide

<img src="images/screenshot.png">

## Features

* Code completion
* Git integration using [fugitive](https://github.com/tpope/vim-fugitive)
* [NERDTree](https://github.com/scrooloose/nerdtree) file browsing
* Quickly find files, buffers etc using [CtrlP](https://github.com/kien/ctrlp.vim)
* Clear trailing whitespace
* vim-airline status bars (with git support)
* Tab completion using [supertab](https://github.com/ervandew/supertab)
* Tab completion in search field ([SearchComplete](https://github.com/vim-scripts/SearchComplete))
* Code tag bar support ([Tagbar](http://majutsushi.github.io/tagbar/))
* Support for Python virtualenvs ([vim-virtualenv](https://github.com/jmcantrell/vim-virtualenv))
* Easy management of surrounding characters (eg. `echo "Hello world"`) using [surround](https://github.com/tpope/vim-surround)

Included colorschemes:

- Tomorrow
- Tomorrow-Night
- Tomorrow-Night-Blue
- Tomorrow-Night-Bright
- Tomorrow-Night-Eighties
- molokai
- solarized (dark and light)
- vividchalk

Supported languages:

* Markdown
* Node.js
  - JSHint
* Python
  - Pylint

## Requirements

- `vim` (7.4 or above)
- `git`
- `ruby`
- `gcc`
- `ctags` (if you're on a Mac, install `ctags` via [Homebrew](http://brew.sh/))

## Usage

### Shortcuts

#### File browsing

- `, + d` - Open the file browser side bar (via [NERDTree](https://github.com/scrooloose/nerdtree))
- `, + f` - Show the current file in the file browser (via [NERDTree](https://github.com/scrooloose/nerdtree))
- `ctrl + p` - Quickly find files, buffers etc using [CtrlP](https://github.com/kien/ctrlp.vim)
- `shift + T` - Open file in new tab from the file browser

#### Tag side bar

- `, + T` - Toggle tag bar ([Tagbar](http://majutsushi.github.io/tagbar/))

### Git integration

Git integration is provided via the [fugitive](https://github.com/tpope/vim-fugitive) plugin. Below are some common examples.

**Status**

    :Gstatus

**Commit (all)**

    :Gcommit
    :Gcommit -a

**Diff**

    :Gdiff

**Push**

    :Gpush origin master

### CoffeeScript

Vinter supports CoffeeScript syntax, compiling, linting and indenting (via [vim-coffee-script](https://github.com/kchmck/vim-coffee-script)). Check their [documentation](https://github.com/kchmck/vim-coffee-script) for details on how to compile and lint your code.

### Surround

You can use any command from the [vim-surround](https://github.com/tpope/vim-surround) package. For example:

#### Change surrounding charaters

You can change surrounding characters with the `cs` command.

**Example**

Replace the `"` with `'` in this string by typing `cs"'`:

    echo "Hello world"

Becomes

    echo 'Hello world'

#### Delete surrounding characters

You can delete surrounding characters with the `ds` command.

**Example**

Delete `"` by typing `ds"`:

    echo "Hello world"

Becomes

    echo Hello world

#### Surround a specific word

You can add surroundings to a specific word with the `ysiw` command.

**Example**

Add `[` around `Hello` by moving the cursor to `Hello` and the type `ysiw[`:

    echo Hello world

Becomes

    echo [ Hello ] world

#### Surround a whole line

You can change the surrounding on a whole line with the `yss` command.

**Example**

Add `{` around a line by typing `yss{`

    echo "Hello world"

Becomes

    { echo "Hello world" }


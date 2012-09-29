## Taboo.vim

**v0.1.1**

Taboo is a simple plugin for easily customize and rename tabs in vim. 


### Installation

Vim version 7.3 is required.

Install into `.vim/plugin/taboo.vim` or better, use Pathogen.

**NOTE**: tabs look different in terminal vim than in gui versions. If you wish
having terminal style tabs even in gui versions you have to add the following
line to your .vimrc file:  

```
set guioptions-=e
```


### Mappings

* `<leader>tt`: Rename the current tab.
* `<leader>to`: Open a new tab and ask for its name.
* `<leader>tr`: Reset the tab name to its default.


Set the following if you want prevent the plugin to set these mappings for you:

```
let g:taboo_enable_mappings = 0
```

To set your own mappings, refer to the following available commands:

* `TabooRenameTab <arg>`: Renames the current tab with the name provided.
* `TabooRenameTabPrompt`: As above but asks for the name via prompt. 
* `TabooOpenTab <arg>`: Opens a new tab and and gives it the name provided. 
* `TabooOpenTabPrompt`: As above but asks for the name via prompt.
* `TabooResetName`: Removes the custom label associated with the current tab.


### Settings

* `g:taboo_format`: With this option you can customize the way normal tabs (not
  renamed tabs) are displayed. Below all the available items that can be used: 

    - `%f`: file name
    - `%F`: path relative to $HOME
    - `%a`: absolute path
    - `%[n]a` : custom level of path depth
    - `%n`: show tab number only on the active tab
    - `%N`: show always tab number
    - `%m`: modified flag
    - `%w`: number of windows opened into the tab

    default: `%f%m` 

    **NOTE**: in renamed tabs, the items `%f`, `%F`, `%a` and `%[n]a` will be avaluated to the custom label associated to that tab.

* `g:taboo_format_renamed`: Same as `g:taboo_format` but for renamed tabs.

    default: `[%f]%m` 

For other commands and settings type `:help taboo.txt`


### Changelog

* **v0.1.1**: added gui support and simplified installation
* **v0.1.0**: first stable release

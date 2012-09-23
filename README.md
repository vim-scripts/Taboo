## Taboo.vim

Taboo is a simple plugin for easily cutomize and rename tabs in **terminal vim**. 


### Installation

Install into `.vim/plugin/taboo.vim` or better, use Pathogen.

To complete the installation be sure to add the following lines to your `.vimrc` file:

```
set tabline=%!TabooTabline()
set showtabline=1   " set to 2 if you want the tabline to always be visible
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

* `g:taboo_format`: With this option you can customize the way normal tabs (not renamed tabs) are displayed. Below all the available items that can be used: 

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

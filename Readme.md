All of the modules require a current version of [CoreScripts](https://github.com/TES3MP/CoreScripts).

You can find a recommended way of setting up your server here [ServerSetup.md](ServerSetup.md).

To install any of the modules, go to your `scripts/custom/` folder and clone its repository there.  
Then add a `<repo-name> = require("custom.<repo-folder>.main")` line to your `customScripts.lua`.  
Here `<repo-name>` stands for the name of the repository and `<repo-folder>` for the directory you cloned it to (same by default).

It is worth noting that the order of `require`s in `customScripts.lua` is important, some of my modules will mention some specific requisitions.
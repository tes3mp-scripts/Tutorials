All of the modules require a current version of [CoreScripts](https://github.com/TES3MP/CoreScripts).

You can find a recommended way of setting up your server here [ServerSetup.md](ServerSetup.md).

To install any of the modules, go to your `scripts/custom/` folder and clone its repository there.  
For some modules it is necessary to clone them into the default folder (same as their name, e.g. without providing a second argument to `git clone`).  
Then add a `<repo-name> = require("custom.<repo-name>.main")` line to your `customScripts.lua`.  
Here `<repo-name>` stands for the name of the repository.  
You can then update a module simply by doing a `git pull` and in come cases deleting/changing relevant files in `data/custom/`, if their format has changed.

It is worth noting that the order of `require`s in `customScripts.lua` is important, some of my modules will mention specific dependencies.
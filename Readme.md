All of the scripts require the current version of [CoreScripts](https://github.com/TES3MP/CoreScripts).

You can find a recommended way of setting up your server here [ServerSetup.md](ServerSetup.md).

To install any of my scripts:
1. Go to the script's repository ([DataManager](https://github.com/tes3mp-scripts/DataManager) as an example)
2. Download the files. There are two ways to do so:
    1. Using git (recommended, get it here https://git-scm.com/downloads):
        1. Navigate to your `server/scripts/custom` folder
        2. Open a powershell window in that folder (`shift + right click` on empty space)
        3. Copy the https git command from the script's repository (green button which says `Code`)
        4. Paste it into your powershell window (`right click`) and press `Enter`
        5. If you need to update the script in the future, simply open the powershell window again and run `git pull origin master`  
            Keep in mind that there might be breaking changes to the configuration/data files  
            Make sure you can rollback in case you run into issues, run `git log` before `git pull` and remember the last `commit hash`, which looks something like `53758ef` or `53758efebceaaab340b8611d53ca5f9d4a8ed88c`
            To reset to an older version, run `git reset <commit-hash> --hard`
    2. Download as a zip file:
        1. Open the code download menu on the script repository page (green button which says `Code`)
        2. Click `Download ZIP`
        3. Unpack the archive into a folder (e.g. `DataManager-master`)
        4. Rename that folder to remove the branch name (e.g. from `DataManager-master` to `DataManager`)
        5. Copy this folder into your `server/scripts/custom` folder
3. Add a to your `server/scripts/customScripts.lua`:  
    For most scripts, simply `require`-ing its `main.lua` is enough. For example:
    ```Lua
    require('custom.VisualHarvesting.main')
    ```
    But if any other scripts depend on it (that's the case with many of my scripts), you also need to assign the result to a global variable:
    ```Lua
    DataManager = require('custom.DataManager.main')
    ```
    Keep in mind that the order of `require`s in `customScripts.lua` is important, if a script depends on another, it should be `require`d after it
4. Most scripts also include a configuration file:  
    After the first time you launch the server with the script enabled, a json configuration file will be generated inside `server/data/custom/`  
    You can edit this file manually to alter that script's behaviour
5. Some scripts might also generate data files in the same folder (`server/data/custom`):  
    Usually you are not supposed to change them manually (other than just delete them to reset the script's data), but if there is an exception, the script's page will mention it
6. All of my scripts expect you to close your server correctly:  
    On Linux, you can achieve that by sending `\n` (pressing `Enter`) in the server window  
    On Windows, you can use my [ShutdownServer](https://github.com/tes3mp-scripts/ShutdownServer) script

# Install tes3mp

Get the latest `0.7` release at https://github.com/TES3MP/openmw-tes3mp/releases.  
Unpack it to a folder of your choice.

# Update CoreScripts

Keep in mind that you should be using the latest tes3mp build to ensure current CoreScripts function properly. 

1. Find the `server` folder inside your installation.
2. Back up this folder (e.g. simply rename it to something that's not `server`).
3. Clone the [CoreScripts repository](https://github.com/TES3MP/CoreScripts) into `server` directory inside your installation, such as by running the following command in your tes3mp insallation folder:  
    `git clone https://github.com/TES3MP/CoreScripts.git server`.
4. Go to the folder you kept in step 2 and copy all its contents into `server`. Skip any files that already exist.
5. If you've edited `config.lua` or `customScripts.lua`, copy them from the backup folder, and overwrite the default ones in the new `server` folder

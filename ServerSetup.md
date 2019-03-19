Install tes3mp
---
Get the latest `0.7` release at https://github.com/TES3MP/openmw-tes3mp/releases.

Unpack it to a folder of your choice.

Update CoreScripts
---
1. Find the `server` folder inside your installation. It might be called `mp-stuff` on Windows, or whatever your `home` value is in `tes3mp-server-default.cfg`.
2. Backup this folder (e.g. simply rename it).
3. Clone the [CoreScripts repository](https://github.com/TES3MP/CoreScripts) into `server` directory inside your installation. `git clone https://github.com/TES3MP/CoreScripts.git server`
4. Go to the folder you kept in step 2 and copy all its contents into `server`. Skip any files that already exist.
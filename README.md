# multicraft-confs

Multicraft jar.conf files for simplifying server setups

## Installation Instructions

The best way to use this repo is to download the zip for the archive and upload to the jar folder
 of your server and unzip into the jar folder, this will put the conf files where you want them
 and put the forge_store folder with the libraries in the right place.

 Then you need to go into multicraft settings and update the files for the version you want to use,
  then create you server, set your server base dir to a memorable name and start your server, the server
  will crash but thats ok. Stop your server.

  Now copy the relevant library and server from forge_stores into your servers base directory, then chown
  the copied libraries folder recursively to the server user ie

            chown -R mc3:mc3 libraries

   Now do the same for the minecraft_server-1.11.2.jar whatever.

Now the last thing you need to do is to copy the minecraft-forge-1.11.2.jar file
also to your server base directory and chown that too.

And thats it you can start the server it it will load.

The conf files are set to run the forge jar from your server base directory, this
way we can have multiple forge servers on a multicraft panel

## Helper

There is now a helper file called mover, after extracting the archive to your jar folder, use

        chmod +x mover

Now when you need to setup a server, just use

        ./mover 1.11.2 myserver

and it will move all the files automatically, however you do have to have been in to multicraft and updated the jat and conf in settings>update minecraft first or it wont find the correct jar file fo copy for forge

## LazyBri commit

I have created a "custom.jar.conf",made specially for OmniFactory-dev,I will periodically upload and replace the "/forge_stores/custom/custom.jar" according the dev-release of OmniFactory,normal user can download this repo and replace the "custom.jar" according to their use.

## Usage & explanation of "mover-custom"

Usage:
        ./mover-custom myserver
***"myserver" is the dirctory of your server root dir.***

Explanation:
This shell script is edited to only copy "custom.jar" into your server folder,so only gave it your server's dirctory, then it will do the job for you.
  **Scrpit Origin:<https://github.com/ronappleton/multicraft-confs/mover>**

## OmniFactory-Dev jar version

***This will change with each update***

Now is **dev-2dd8f8a**

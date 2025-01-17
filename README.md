# Beat!Station
[![Build Status](https://api.travis-ci.org/Beat-Station/Beat-Station.svg?branch=master)](https://travis-ci.org/Beat-Station/Beat-Station)
[![Average time to resolve an issue](http://isitmaintained.com/badge/resolution/Beat-Station/Beat-Station.svg)](http://isitmaintained.com/project/Beat-Station/Beat-Station "Average time to resolve an issue")
[![Percentage of issues still open](http://isitmaintained.com/badge/open/Beat-Station/Beat-Station.svg)](http://isitmaintained.com/project/Beat-Station/Beat-Station "Percentage of issues still open")

[![forthebadge](http://forthebadge.com/images/badges/60-percent-of-the-time-works-every-time.svg)](http://forthebadge.com)
[![forthebadge](http://forthebadge.com/images/badges/contains-technical-debt.svg)](http://forthebadge.com)
[![forthebadge](http://forthebadge.com/images/badges/fuck-it-ship-it.svg)](http://forthebadge.com)

[Website](beat.misterio7.com/) - [Code](https://github.com/Beat-Station/Beat-Station) - [Discord](https://discord.gg/JVbQmS3)

It's based on [Paradise Station](https://github.com/ParadiseSS13/Paradise) and [Goon Station](https://github.com/goonstation/goonstation-2016) - This is the customized code we use at Brazilian Station server on BYOND. I've made some modifications, so i'm uploading the source. Enjoy.

# Information
This is a code used in a Brazilian server. Everyone is welcome to contribute though.
I'm currently using music from Kevin MacLeod and SiriusBeat. Licenses are on the bottom of the file.

# Getting the code
The more complicated and easier to update method is using git.  
You'll need to download git or some client from [here](http://git-scm.com/).  
When that's installed, right click in any folder and click on "Git Bash".  
When that opens, type in:

    git clone https://github.com/Beat-Station/Beat-Station

(hint: hold down ctrl and press insert to paste into git bash)

This will take a while to download, but it provides an easier method for updating.

### INSTALLATION

First-time installation should be fairly straightforward.  
First, you'll need BYOND installed.  
You can get it from [here](http://www.byond.com/).

This is a sourcecode-only release, so the next step is to compile the server files.  
Open paradise.dme by double-clicking it, open the Build menu, and click compile.  
This'll take a little while, and if everything's done right,
you'll get a message like this:

    saving paradise.dmb (DEBUG mode)

    paradise.dmb - 0 errors, 0 warnings

If you see any errors or warnings,
something has gone wrong - possibly a corrupt download or the files extracted wrong,
or a code issue on the main repo.  Ask on IRC.

Once that's done, open up the config folder.  
You'll want to edit config.txt to set your server location,
so that all your players don't get disconnected at the end of each round.
It's recommended you don't turn on the gamemodes with probability 0,
as they have various issues and aren't currently being tested,
so they may have unknown and bizarre bugs.

You'll also want to edit admins.txt to remove the default admins and add your own.  
"Host" is the highest level of access, and the other recommended admin levels for now are
"Game Admin" and "Moderator".  The format is:

    byondkey - Rank

where the BYOND key must be in lowercase and the admin rank must be properly capitalised.  
There are a bunch more admin ranks, but these two should be enough for most servers,
assuming you have trustworthy admins.

Finally, to start the server,
run Dream Daemon and enter the path to your compiled paradise.dmb file.  
Make sure to set the port to the one you specified in the config.txt,
and set the Security box to 'Trusted'.  
Then press GO and the server should start up and be ready to join.

---

### UPDATING

To update an existing installation, first back up your /config and /data folders
as these store your server configuration, player preferences and banlist.

If you used the zip method,
you'll need to download the zip file again and unzip it somewhere else,
and then copy the /config and /data folders over.

If you used the git method, you simply need to type this in to git bash:

    git pull

When this completes, copy over your /data and /config folders again, just in case.

When you have done this, you'll need to recompile the code, but then it should work fine.

---

### Configuration

For a basic setup, simply copy every file from config/example to config.

---

### SQL Setup

The SQL backend for the library and stats tracking requires a MySQL server.  
Your server details go in /config/dbconfig.txt,
and the SQL schema is in /SQL/paradise_schema.sql or /SQL/paradise_schema_prefix.sql,
depending on if you want table prefixes.  
More detailed setup instructions are located on /tg/station's wiki: http://www.tgstation13.org/wiki/Downloading_the_source_code#Setting_up_the_database

---

### IRC Bot Setup

Included in the repo is an IRC bot capable of relaying adminhelps to a specified IRC
channel/server (thanks to Skibiliano).  
Instructions for bot setup are included in the /bot/ folder,
along with the bot/relay script itself.

### LICENSE

Beat!Station is licensed under the GNU Affero General Public License version 3.
As of 5th January 2015 any new contributions are licensed under the AGPL as well,
if you wish to submit code under the GPL v3 then commits and files must be marked as such
in comments. If you wish to use our code in a closed source manner you may use anything
before commit 445615b8439bf606ff204a42c8e7b6b69d983255 on [Paradise](https://github.com/ParadiseSS13/Paradise),
which is licensed under GPL v3.
The major change here is that if you host a server using any code licensed under AGPL you
are required to provide full source code for your servers users as well,
including addons and modifications you have made.

See [this](https://www.gnu.org/licenses/why-affero-gpl.html) for more information.

Any files located in the `Paradise/icons/goonstation` and `Paradise/sound/goonstation`
folders, and any of their subdirectories, are licensed under the
Creative Commons 3.0 BY-NC-SA license
(https://creativecommons.org/licenses/by-nc-sa/3.0)

All other assets including icons and sound files are licensed under the
Creative Commons 3.0 BY-SA license (https://creativecommons.org/licenses/by-sa/3.0/),
unless otherwise indicated.

Credits for songs used:

Thunderbird Kevin MacLeod (incompetech.com)
Licensed under Creative Commons: By Attribution 3.0 License
http://creativecommons.org/licenses/by/3.0/

"Floating Cities"
Kevin MacLeod (incompetech.com)
Licensed under Creative Commons: By Attribution 3.0
http://creativecommons.org/licenses/by/3.0/

Orion 300XB Kevin MacLeod (incompetech.com)
Licensed under Creative Commons: By Attribution 3.0 License
http://creativecommons.org/licenses/by/3.0/

Myst on the Moor Kevin MacLeod (incompetech.com)
Licensed under Creative Commons: By Attribution 3.0 License
http://creativecommons.org/licenses/by/3.0/

Music by: Sirius Beat - Tronicles
Link: http://youtu.be/zIRo7NJ4uLE

If any producer or label has an issue with me using your work, please contact me so i can remove it!


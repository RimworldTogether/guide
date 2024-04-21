# Getting Started

We'll explain the process on how to setup your own server in this page.

To get started, you can start by installing the [server files](https://github.com/RimworldTogether/Rimworld-Together/releases/latest). Choose the appropriate version for your operation system, either Linux or Windows. We do not currently offer support for mac OS nor do we plan to in the future.

## QuickStart
This guide will assume you're running a windows installation.

Start by creating a folder on your desktop and extracting the server inside of it, you should now be able to launch the server.

A bunch of files should have been created, and a terminal window should have popped up. From there, the server should be up and running. You can now join your server through the in game menu, please refer to our client guide for more information.

The first client to join the server will be responsible for creating the world. We heavily recommend only generating the world with the minimum enforced modlist (see how to add enforced mods bellow) to avoid any problems.

## Configuration
Most of the files can be ignored, the relevant ones are listed bellow.

### Dlcs
You can find the dlc files on our [https://github.com/RimworldTogether/Rimworld-Together github page] for server side use only.

Dlcs are considered mods, so you can treat them as mods. 

### Mods
The first thing you probably want to configure are your mods. Currently, you can have enforced, optional or forbidden:

*Enforced mods will be required for connection. Otherwise, the client will not be able to connect
*Optional mods are not required for connection and the client will be able to connect without them
*Forbidden mods are banned, which means the client will not be able to connect with them. Useful for servers without any mods restriction.

You can find your mod files in your workshop folder, usually located in your steam folders under C:\Program Files (x86)\Steam\steamapps\workshop\content\294100.

You can use this [https://github.com/Byte-Nova/Library/releases/latest tool] to rename your mods to their in game name instead of ids. '''<u>Make sure to use it on a copy of your mods, not you actual workshop folder.</u>'''

We heavily recommend to have any mods that affect the world map or factions to be enforced, as they can break things otherwise.

You can find a list of our current incompatibility list [https://docs.google.com/spreadsheets/d/14f4oJIV82SzqNK-Tyewr0OKxVRgge8xFasivACwRlsA/edit#gid=0 here].

### Core

#### ActionValues
You can change the cost in silver of actions in this file. Currently, you can use them on players.

#### DifficultyValues
You can set all the values for your enforced difficulty if are currently using that configuration. You can find all those stats under the custom storyteller option in Rimworld.

#### EventValues
You can change the cost in silver of events in this file. You can call those events on players.

#### ServerConfig
You can change various settings about the server, such as:

* The port being used by the server
* The ip being used by the server (when in doubt, leave it to `0.0.0.0`)
* The maximum amount of players connected at once.
* The maximum amount of time a client can go without responding the server in milliseconds. You can increase it if you have an unstable connection.
* Verboselogs gives you additional logging information on the server
* DisplayChatInconsole does just that, the in game chat will be displayed on the console.

#### ServerValues
You can change if you want to allow custom scenarios for clients (ex :crashlanded, mechanitor, naked brutality).

#### SiteValues
You can change the various cost and production of sites in this file. You can find out more information about sites on our [[Sites|site page]].

#### Whitelist
The file lets you configure if you want a whitelist or not. Simply put the in game usernames (the one used to log in) in between the brackets.

#### WorldConfig
This file stores all the world data. We do not recommend editing it mid run.

## Making your server public

### Port forwarding
Port forwarding can be a little complicated. We'll assume you have basic knowledge of computers in this section.

* Start by opening a command prompt
* Type ipconfig and search for your default gateway.
* Enter your default gateway in your browser
* Find your router's settings
* Find port forwarding (might be under advanced settings)
* Create a new rule with the port that the server is using
* Select TCP or Both for the port forwarding type. 
* Select your computer if required.
* Your friends should be able to connect to your server using your public ip and port! Make sure your server is running and that you saved the rule.

### Virtual private network (VPN)
Vpns such as Radmin, hamachi or wireguard can be used to share your server with a group of friends. Keep in mind this option isn't recommended for large servers.

We'll be using Radmin in our example down bellow:

* Download Radmin from https://www.radmin-vpn.com/
* Press the power button on the app to turn it on, and create a new network with a unique password and name
* Your friends can now join that network trough Radmin, and connect to the server with the port and the vpn's ip, which you can get by right clicking on your computer in the radmin application.

## TroubleShooting
For additional help with troubleshooting, please join our discord server at https://discord.gg/VFFSvfJTQD.

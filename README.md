<div align="center">

<img src="Logo/GC_Logo.png" alt="Logo" width="500"/>

[![GitHub release](https://img.shields.io/github/release/Buff-oG/GC-Server-Conf-Template.svg?style=flat-square)](https://github.com/Buff-oG/GC-Server-Conf-Template/releases)

# Galactic Contention Server Template

### Configuration template for the mod Galactic Contention running on Squad.

<br><br>

The files were edited to be as much flexible as possible.

The value " **$word** " mean it's a variable. You must change it to your need.

You must put the configuration files inside your ServerConfig directory:
<br>
```C:\$InstallationFolder\SquadGame\ServerConfig\```

<br>

### You will need to edit particular files such as:


#### --- *Administration* ---

[Server.cfg](https://github.com/Buff-original/GC-Server-Conf-Template/blob/main/ServerConfig/Server.cfg) --> *Edit your server name*

[MOTD.cfg](https://github.com/Buff-original/GC-Server-Conf-Template/blob/main/ServerConfig/MOTD.cfg) --> *Edit your Message Of The Day*

[ServerMessages.cfg](https://github.com/Buff-original/GC-Server-Conf-Template/blob/main/ServerConfig/ServerMessages.cfg) --> *Edit your heads up messages*

[Admin.cfg](https://github.com/Buff-original/GC-Server-Conf-Template/blob/main/ServerConfig/Admins.cfg) --> *Add your necessary users*

<br>
<br>
#### --- *Levels and Layers selection and informations* ---

[_CompleteLayerList.cfg](https://github.com/Buff-oG/Galactic-Contention-Server-Template/blob/main/ServerConfig/_CompleteLayerList.cfg) --> *The entire Galatic Contention Layer list. Feel free to pick your layers from this configuration file.*

[_CompleteLevelIds.cfg](https://github.com/Buff-oG/Galactic-Contention-Server-Template/blob/main/ServerConfig/_CompleteLevelIds.cfg) --> *The entire Galatic Contention Level list. Feel free to pick your Level from this configuration file.*

<br>
<br>
#### --- *Levels/Layers settings for standard rotation* ---

[LayerRotation.cfg](https://github.com/Buff-original/GC-Server-Conf-Template/blob/main/ServerConfig/LayerRotation.cfg) --> *Specify which layer you would like to add or remove from the layer rotation.*

[LevelRotation.cfg](https://github.com/Buff-original/GC-Server-Conf-Template/blob/main/ServerConfig/LevelRotation.cfg) --> *Specify which level you would like to add or remove from the map rotation.*

[_ServerWithStandardRotation.cfg](https://github.com/Buff-oG/Galactic-Contention-Server-Template/blob/main/ServerConfig/_ServerWithStandardRotation.cfg) --> *Server configuration with standard layer rotation. Map voting is not enabled.*
<br>
<br>
#### --- *Levels/Layers settings for the map vote configuration* ---

[LayerVoting.cfg](https://github.com/Buff-oG/Galactic-Contention-Server-Template/blob/main/ServerConfig/LayerVoting.cfg) --> *Specify the layers you would like to have in your map vote pool. We recommend to put the big layers such as AAS, RAAS, INV, RINV and Disturbance (Insurgency).*

[VoteConfig.cfg](https://github.com/Buff-oG/Galactic-Contention-Server-Template/blob/main/ServerConfig/VoteConfig.cfg)  --> *Specify your map vote configuration such as, the amount of layers, faction selection, game modes, etc.*

[LayerVotingLowPlayers.cfg](https://github.com/Buff-oG/Galactic-Contention-Server-Template/blob/main/ServerConfig/LayerVotingLowPlayers.cfg) --> *Specify the low population layers you would like to have in your map vote pool. We recommend to put small maps, Skirmish and Seed layers.*

[ExcludedLayers.cfg](https://github.com/Buff-oG/Galactic-Contention-Server-Template/blob/main/ServerConfig/ExcludedLayers.cfg) --> *Specify the layers you do not want to be part of your map vote pool. We recommend to exclude broken layers if you find any.*

[ExcludedLevels.cfg](https://github.com/Buff-oG/Galactic-Contention-Server-Template/blob/main/ServerConfig/ExcludedLevels.cfg) --> *Specify the Level id that you do not want to be part of your map vote pool. We recommend to exclude broken layers. By default the Galactic Contention team already commented out the levels that we do not recommend to put on LIVE play.*

<br>
<br>

## Misc

Steam MOD ID: 2428425228

Steam Workshop URL: https://steamcommunity.com/sharedfiles/filedetails/?id=2428425228
 
Any errors on maps with the "_DEV or "_WIP" extension is not supported in Discord "#bug-report" nor on GitHub. These levels and layers are for test purposes only.

Make sure to copy these files into the proper directory! If you have any questions, feel free to create an issue.

---
description: Tweaks and tricks to improve both your experience in hosting and others' in playing on your server
---

# Best practices

{% hint style="info" %}
TODO: If you have experience in hosting Northstar servers and want to share your knowledge, please open a [pull request](https://github.com/R2Northstar/NorthstarWiki/pulls).
{% endhint %}

## Optimization Commands (Optional)

| Command                          | Description                                                                                                                    |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| `net_compresspackets 1`          | Enable compress packets                                                                                                        |
| `net_compresspackets_minsize 64` | Decrease usage from ~12-16 mbps to ~6-8 mbps on 20 player PVP server and ~9-12mbps to ~5-7 mbps on 12 player gun game server   |
| `sv_maxrate 127000`              | Sets the maximum bandwidth rate allowed (both incoming/outcoming) per second (in bytes)                                        |

**Note:** The effect is dependent on your network, system, etc. Therefore, you should really add the command one by one and test it to see if there is any benefit for your server.

## Reducing file size

When hosting a server, you don't need all of the game's assets. This means that, without doing anything, there is a lot of unused space simply sitting there.

You can delete the following files and still be able to host a Northstar server:

- vpk/client_sp_* englishclient_sp_*
- r2/maps
- r2/cfg/*.ekv
- r2/paks/ except for {patch_master,{common,common_mp}{,\(*}}.rpak ui*
- r2/sound/**
- r2/media
- r2/screenshots
- bin/x64_retail/{client,auditionwin64}.dll
- bin/dxsupport.cfg
- platform
- Titanfall2.exe
- on wine without origin installed:
        - Core
        - Support
        - __Installer

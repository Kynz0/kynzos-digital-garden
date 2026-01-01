---
{"dg-publish":true,"permalink":"/syncthing/","created":"2025-11-13T23:04:06.610+01:00","updated":"2026-01-01T02:40:29.408+01:00"}
---

[Syncthing](https://syncthing.net/) is a FOSS peer-to-peer file synchronization utility and I'm using it to sync my [[Obsidian\|Obsidian]] notes between my pc and my phone.

# Fedora setup:
- Install Syncthing: `sudo dnf install syncthing`
- Start it by running the new menu entry "Start Syncthing" (it just executes `syncthing serve --no-browser --logfile=default`)
- Access the UI on http://127.0.0.1:8384 (or by running the newly added "Syncthing Web UI" menu entry)
- Add a folder and type in the folder path to your Vault
- Actions > Show ID and scan the ID with your phone, then click accept or whatever to connect the device
- Click on your folder > Edit > Sharing > check the box next to your device
- Run this command to make it work outside of the network: `sudo firewall-cmd --zone=public --add-service=syncthing --permanent` reload after: `sudo firewall-cmd --reload`

# Android setup:
- Install the [Syncthing-fork](https://f-droid.org/en/packages/com.github.catfriend1.syncthingfork/) (or any other fork that you like)
- Give the app all the permissions it asks for
- Click the icon at the top-right corner to add a device
- Click the QR icon right to the ID field to scan the QR code from the pc
- Accept the folder and place it somewhere (e.g. Documents)
- Open Obsidian and select the local folder
- If it is inconsistent then enable it in the battery settings so it can run whenever
---
layout: page
title: Troubleshooting
permalink: /troubleshooting/
nav_order: 5
---

## Steam PC Version

### Crashing on Start
- Try Disabling the Steam Overlay
    1. Right click on the Library entry or click on the Gear icon after selecting the Library entry
    2. Select "Properties" in the drop down menu
    3. In the "General" section of the "Properties" menu, toggle off the "Enable the Steam Overlay while in-game" option
- Try Running the Executable Directly
    1. Right click on the Library entry or click on the Gear icon after selecting the Library entry
    2. Highlight the "Manage" section in the drop down menu
    3. Select the "Browse Local Files" option to open a file explorer window
    4. Run the "tensor.exe" executable file directly

### General Low Performance
- Try Disabling Steam Overlay
    1. Right click on the Library entry or click on the Gear icon after selecting the Library entry
    2. Select "Properties" in the drop down menu
    3. In the "General" section of the "Properties" menu, toggle off the "Enable the Steam Overlay while in-game" option
- Try Turning Off Dynamic Lighting
    1. Select "Options" in the Main Menu
    2. Select the "Video" tab in the Options menu
    3. Select the "Lights" option button and set to "Local Lights Disabled"

### Cannot Connect to Online Multiplayer

{: .warning }
> There is always an inherent security risk in connecting to other computers. Do not connect with computers you do not recognize and trust.

- Try enabling Universal Plug and Play (UPnP)
    1. If your your router is set to use UPnP, the game can be set attempt to automatically port forward through UPnP by checking the "Attempt Port Forwarding via UPnP" option in the "Create Game" Versus menu.
    2. See [this guide](https://www.computerhope.com/issues/ch001367.htm) to set up UPnP.
    3. WARNING: UPnP is considered insecure and should generally be disabled.

- Try setting up Port Forwarding manually
    1. See [this guide](https://stevessmarthomeguide.com/understanding-port-forwarding/) to set up Port Forwarding manually.

## Web Browser (Demo) Version

### Unable to Run
- Check if Web Browser is compatable
    1. Browser requires support for WebAssembly, WebGL, and SharedArrayBuffer

### General Low Performance
- Try Turning Off Dynamic Lighting
    1. Select "Options" in the Main Menu
    2. Select the "Video" tab in the Options menu
    3. Select the "Lights" option button and set to "Local Lights Disabled"

## Contact
More detailed requests for help can be sent to [contact.magentagrid@gmail.com](mailto:contact.magentagrid@gmail.com)

General tips when requesting help:
- Provide as many details as possible
- Provide steps to reproduce the issue, if possible
- Provide screenshots of the issue, if possible
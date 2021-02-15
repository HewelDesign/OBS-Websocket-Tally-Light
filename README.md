# OBS-Websocket-Tally-Light-Alpha-1.1
This small "webpage" connects to any OBS instance on the local network and displays either the stream status (live/offline) or tally information for different scenes or sources(on air/in preview/neither).

## Setup

There is not that much to set up:

 - Install the awesome  [obs-websocket plugin](https://github.com/Palakis/obs-websocket/releases)  by Palakis (Version >= 4.7.0)

    
-   Open the "Tools" menu and select "websocket server settings"
    
-   Make sure that "Enable Websocket server" is checked, "Server Port" is 4444 and "Enable authentification" is unchecked
    
-   Download this repository and unpack or clone it
	
	|α 1.1 | ~~Download MediFire~~ | ~~Dowload Google Drive~~  |.............soon

	|α 1.1 | [Download MediFire](http://bit.ly/3tUOsBs) | [Dowload Google Drive ](http://bit.ly/3aPCNeh) |.............new

	|~~α 1.0~~ | ~~Download MediFire~~ | ~~Dowload Google Drive~~  |.............Old
    

By default it is setup to connect to the IP of the machine you run it on(127.0.0.1). You can change that default start value by editing the IP address and/or the port in line 85 (Pages/Tally.html). You can also change the scriptlink in line 85 (Pages/Script.html).You can open the file directly with a webbrowser or use a  [simple webserver](https://www.apachefriends.org/de/index.html)  somewhere on the network to serv it to local clients. This tool does NOT need an any internet connection to work.

## Features
 - [x] OBS-Websockt plugin
 - [x] Script funtion 
 - [x] Digital clock
 - [x] Online offline tally
 - [ ] Livestream Viewer (in progress)

## General Usage

-   Open the Index.html in a web browser (On a pc, laptop, tablet, smartphone)
-   Press the "Tally" button
-   You can change the ip here to the address of your obs machine. If you edited it in the file as mentioned above it will show up here already filled in.
-   Click on the "Connect Websocket" button
-   If the connection to the obs machine was successful, a list of buttons will show up with all your scenes and sources from obs and another button on top called "Stream Status"
### Show Stream Status

-   Click the "Stream Status" button
-   That's it. It will show OFFLINE and a black background if you're not streaming and LIVE with a red background when the stream is live


### Show Scene Tally

-   Click on the scene name you want that are listed under "Scenes"
-   It will show the name of the scene on top of the page.
-   If the scene is neither in preview or program, the background will be black
-   If the scene is in preview, the background will be green
-   If the scene is in program, the background will be red
-   If a transition (like a fade) is started where the destination scene is the scene you selected, then it will light up red
-   If studio mode is disabled there will be only a red and black display, no green
### Show Source Tally

You can also show the tally status for individual sources. Every scene that containes that source will be handled like described in Show Scene Tally above. The page will update the scenes every 30 seconds in case you add the source to a new scenes after starting the tally. But i recoment to reload the page.

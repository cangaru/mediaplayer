# mediaplayer
light weight media player using TCL/TK and GSTREAMER
Compiled on Ubuntu 18.04 x64. but source and compile script are included
To compile you will need to install libgstreamer1.0-dev.
This should compile on just about any platform once you have well-installed compiler and gstreamer dev library and you have adjusted the compile script to your platform. (This is all currently set up for linux only)
You may need to install further elements of tcl/tk.
The interface is in spanish only, but it is very straight-forward.
To install, download and then change to the downloaded directory and use ./instalar
The install script attempts to install some dependencies (deb) using apt-get.
The player does not build or use libraries for your media files but is designed to run off directory-based media.
Features: 4 executables: reproductor (the interfaz), tocador (the gstreamer compiled player), mandar (a cli for sending commands to the player) convsegundos (a utility for converting seconds to human friendly time duration)
It will play just about anything since it uses gstreamer's "playbin", so if it fails to play it will probably be just a question of installing gstreamer1.0 plugins. Gstreamer is very versatile and robust and should not cause any problems with a decently configured sound system.
Installs to /usr/local/bin.
To use the CLI: mandar command variable, where command can be: 
    agregar_arch {list of files or url}   # add files from file system or properly formed url
    estado 0                              # get the state of the player in the form of "state volume%"
    limpiar 0                             # delete the entire playlist
    tocar 0                               # begin playing the next item on the playlist
    pausar 0                              # set player to pause or play depending on current state
    parar 0                               # stop playing
    set_pos x                             # set position in stream to x% of the stream total (if known)
    set_vol x                             # set volume to x% of full volume.
Let me know how it goes.

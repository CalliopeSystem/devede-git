# DEVEDE NG #

## WHAT IS IT? ##

Devede NG is a rewrite of the Devede DVD disc authoring program. This new
code has been written from scratch, and uses Python3 and Gtk3. It is also
cleaner, which will allow to add new features in the future.

## INSTALLING DEVEDE NG FROM PKGBUILD ##

First, be sure that you have uninstalling any package with devede. Then, Just type:

    git clone https://github.com/KittehCream/devede-git.git
    cd devede-git
    makepkg -si

Devede NG optionally requires these applications which can improve its functionality

    mplayer - (The Movie Player) Offers video preview functionality.
    mpv - (free (as in freedom) media player) Offers video preview functionality.
    vlc - (VideoLAN Client) Offers video preview functionality.
    brasero - (GNOME disc burning application) Offers direct disc burning functionality.
    k3b - (KDE disc burning application) Offers direct disc burning functionality.
    xfburn - (XFCE disc burning application) Offers direct disc burning functionality.

## USING DEVEDE NG ##

Devede NG is very similar to the old devede, with the
exception that, when creating a DVD disc, there are no more "titles" and
"files". Instead, you just add files to the disc. It also lacks support for Mencoder,
and can use only FFMpeg or AVConv for video conversion.

The current visible changes are quite small in number:

* Now allows to add several files at once
* Now makes better use of multicore systems by parallelizing the conversion of several movie files
* The menu edition is interactive
* Has a new "cut" resizing method, to allow to store as widescreen movies with black bars
* Allows to create Matroska files with H.264 video and MP3 audio
* Allows to use VLC, MPV or MPlayer for preview
* Allows to choose between Brasero, K3B, or Xfburn for burning the discs
* Allows to set properties for several files in one step
* Allows to choose the subtitle colors
* Allows to choose between MP2 and AC3 audio for menus

## THINGS TO DO ##

Some of the future ideas to add to Devede NG are, without an specific order:

* add more backends
* add more output formats
* allow to replace the movie's audio track with one or several MP3 or OGG audio files
* preview of a converted menu

## CONTACTING THE AUTHOR ##

Sergio Costas Rodriguez  
rastersoft@gmail.com  
http://www.rastersoft.com  
https://gitlab.com/rastersoft/devedeng.git

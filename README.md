vanilla-extract
===============

Clone OSM planet and perform bounding-box extracts for routing. Consumes and produces PBF format.

## compiling


You will need zlib and protobuf-c libraries. On ubuntu you can install them from packages:

`sudo apt-get install libprotobuf-c0-dev zlib1g-dev`


You will also need gcc and make if you don't already have them:

`sudo apt-get install build-essential`


Clang is a nice compiler with nice error messages. You may want to install it and modify the CC line of the makefile to use it:

`sudo apt-get install clang`


## usage

Only store the database on a filesystem that supports sparse files (ext3 and ext4 do). Everything goes much quicker on a solid-state disk. 
The program itself should only need a few megabytes of memory but benefits greatly from free memory that the 
OS can use as cache.

To load the database:

`cosm <database_directory> <input.pbf>`


To perform an extract:

`cosm <database_directory> <min_lat> <min_lon> <max_lat> <max_lon>`

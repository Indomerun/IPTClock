##############################################################################################
#  IPTClock, a graphical countdown clock for use with the international physicist's tournament
    Copyright (C) 2016-2017  Albin Jonasson Svärdsby & Joel Magnusson

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.
##############################################################################################

## Purpose ##
This program is written to serve the purpose of a timing and presentation tool
for the international physicist tournament. http://iptnet.info/

It is written in python 3 and is meant to be cross-platform, using tkinter as
GUI control and matplotlib for image and graphics tweaking.


## Dependencies ##
IPTClock has the following dependencies:

Python3 or higher

matplotlib

tkinter

(for a smaller breakdown if you want
to avoid installing the entire modules, please see the imports at the top of
IPTClock.py and Classes/iptclock_classes.py)


## (Optional) Dependencies ##
pyaudio

cx_Freeze  (for creating pre built packages: https://anthony-tuininga.github.io/cx_Freeze/)


## How to run ##
The clock is run in a terminal environment using the command:

python3 IPTClock.py

alternatively it can be run using pre build binaries found under the build folder.
For instance in the case of windows use the exe file IPTClock.exe found in
build/exe.win-ARCHITECHURE-PYTHONVER/IPTClock.exe



## configuration ##
Variables used to change the IPTClock is positioned in Config/config.py

Further, changes to the fight layout in the form of stages and time can
be changed in the file stages.txt


 
## Build instructions ##
The pre built packages is constructed by using cx_Freeze to "freeze" the present
build and creates a separate python environment that can run the program.
You have to perform the building on the operating system you want the build for.
If you use exotic linux builds I can't predict the result ;-)

The built process is started by typing this in the terminal:

python3 setup.py build

Where python3 might be any desired python3 version.
(although see "Known bugs" for some version recommendation)

After build you might have to copy the folder and files containing configurations
to position relative the executable file in the build folder.
(for example stages.txt)


## Known bugs ##
I encountered a problem where the linking was broken while using cx_Freeze and
python 3.5, using python 3.4 solved this issue.


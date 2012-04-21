Return to Castle Wolfenstein single player GPL game source
==========================================================

This file contains the following sections:

GENERAL NOTES
LICENSE

GENERAL NOTES
=============

Game engine:
------------

This release contains only the source of the game DLL files. It was separated
from JLQuake in order to keep it clean and because there are no plans on doing
any improvements on game code. 32 bit game DLLs built from this release should
still be compatible with original engine, but it's recomended to use an improved
game engine such as JLQuake.

Game data and patching:
-----------------------

This source release does not contain any game data, the game data is still
covered by the original EULA and must be obeyed as usual.

You must patch the game to the latest version.

Note that RTCW is available from the Steam store at
http://store.steampowered.com/app/9010/

Linux note: due to the game CD containing only a Windows version of the game,
you must install and update the game using WINE to get the game data.

Compiling on Windows:
---------------------

A Visual C++ 2010 project is provided in src\wolf.sln.
The solution file is compatible with the Express release of Visual C++.

You can test your binaries by replacing qagamex86.dll, cgamex86.dll, uix86.dll
at the top of the RTCW install. 64 bit version file names are qagamex86_64.dll,
cgamex86_64.dll and uix86_64.dll. You'll need a 64 bit version of JLQuake to
run them.

Compiling on GNU/Linux and other UNIX based systems:
----------------------------------------------------

mkdir build
cd build
cmake ..
make

You can test your binaries by replacing qagamei386.so, cgamei386.so, uii386.so
at the top of the RTCW install. 64 bit version file names are qagamex86_64.so,
cgamex86_64.so and uix86_64.so. You'll need a 64 bit version of JLQuake to
run them.


LICENSE
=======

See COPYING.txt for the GNU GENERAL PUBLIC LICENSE

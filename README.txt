Return to Castle Wolfenstein single player GPL source release
=============================================================

This file contains the following sections:

GENERAL NOTES
LICENSE

GENERAL NOTES
=============

Game data and patching:
-----------------------

This source release does not contain any game data, the game data is still
covered by the original EULA and must be obeyed as usual.

You must patch the game to the latest version.

Note that RTCW is available from the Steam store at
http://store.steampowered.com/app/9010/

Linux note: due to the game CD containing only a Windows version of the game,
you must install and update the game using WINE to get the game data.

Compiling on win32:
-------------------

A Visual C++ 2010 project is provided in src\wolf.sln.
The solution file is compatible with the Express release of Visual C++.

You will need to execute src\extractfuncs\extractfuncs.bat to generate src\game\g_save.c

You can test your binaries by replacing qagamex86.dll, cgamex86.dll, uix86.dll at the top of the RTCW install

Compiling on GNU/Linux x86:
---------------------------

Go to the src/unix directory, and run the cons script
(cons is a perl based precursor to scons, this is what we were using at the time)

Run ./cons -h to review build options. Use ./cons -- release to compile in release mode.

If problems occur, consult the internet.

Other platforms, updated source code, security issues:
------------------------------------------------------

If you have obtained this source code several weeks after the time of release
(August 2010), it is likely that you can find modified and improved
versions of the engine in various open source projects across the internet.
Depending what is your interest with the source code, those may be a better
starting point.


LICENSE
=======

See COPYING.txt for the GNU GENERAL PUBLIC LICENSE

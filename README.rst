foobar2000 SDK 1.1
******************

This repository contains a marginally modified foobar2000 SDK, suitable to host the build of awesome components like foo_wave_seekbar.

Requirements
------------
* CMake 2.8.x
* If you need the ``-T`` CMake command line option (for building with the ``v110_xp`` toolset), CMake 2.8.11 is required.
* Boost 1.53, located by the ``BOOST_ROOT`` environment variable.
* Intel TBB, located by the ``TBBROOT`` environment variable.
* DirectX SDK (Feburary 2010), located by the ``DXSDK_FEB10`` environment variable.

Usage
-----
Modify ``foobar2000_sdk\CMakeLists.txt`` to add additional components to compile and install.
::

	mkdir build-fb2k
	cd build-fb2k
	cmake -G "Visual Studio 11" -T v110_xp ..\foobar2000_sdk

Components will be installed into ``build-fb2k/portable/user-components``, making ``build-fb2k/portable`` an excellent place to install a portable foobar2000 installation.
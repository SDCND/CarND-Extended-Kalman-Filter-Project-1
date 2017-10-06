perform these steps to setup your visual studio project:

#1 install cmake

Download and run windows installer
see https://cmake.org/download/

#2 install make

Download setup from http://gnuwin32.sourceforge.net/packages/make.htm
select Complete package, except sources	 Setup
run downloaded setup

#3 clone and install vcpkg
clone from https://github.com/Microsoft/vcpkg:

cd c:\
git clone https://github.com/Microsoft/vcpkg.git
cd vcpkg
call bootstrap-vcpkg.bat

#4 adapt and call the install script for windows

cd to directory ide_profiles\VisualStudio
open install-windows.bat and adjust lines 5 to 7 to the settings you will use when building your Visual Studio project (platform, toolset, buildtype)
you could also pass these settings as command line arguments to install-windows.bat
if you have more than one toolset installed, comment line 14 and uncomment line 15

call install-windows.bat

#5 open solution and adapt toolset settings

open CarND-Extended-Kalman-Filter-Project.sln
open project properties
adapt target platform version and platform toolset for all configurations

#6 build project

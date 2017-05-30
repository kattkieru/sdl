GBDK3

libsdl 1.2.15
=============

This is a direct copy from the official site:
https://www.libsdl.org/release/SDL-1.2.15.tar.gz

I also applied the following patch to make it compile on modern macOS:
https://bugzilla.libsdl.org/show_bug.cgi?id=2085

The CMakeLists.txt file included will bootstrap a static library build.  I wanted to be able to use SDL a bit more easily from within other cmake projects, so this is the result.  

~ k



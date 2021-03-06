RecastNavigationDelphi
======================

Port of Recast Navigation into Delphi 

Source code location:
   https://github.com/memononen/recastnavigation


Source code version:
   Around 01 Nov 2014


Guidelines:
 - RecastNavigationDelphi is a straight clone of RecastNavigation with as little changes as possible, to allow to keep projects synced in the future.
 - RND follows RN structure very closely, except for GUI stuff, which is VCL for simplicity instead of imGUI RN solution.
 - File names are the same, with "RN_" prefix.


Hints about the code:
 - Multi-condition "for" loops and loops where iterator gets changed within, need to be converted to while/repeat. Run the loop code before any "continue".
 - Move method first two arguments (Src, Dst) need to be swapped in Delphi.
 - Delphi needs to wrap overflowing manipulations with a {$O} directive to supress errors.
 - Delphi needs manual disposal of objects created within record , as they dont have built-in destructor support in them.


Todos:
 - Fix plethora of memory leaks around the code.
 - TileMesh and TempObstacles demos.
 - Some parts are commented out, waiting to be ported.

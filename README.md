# Blender-AC3D - Version 3.3

## What is it?
It's a few python scripts to import/export Inivis AC3D data into and out of Blender 2.80.

## How do I install it?
Know that the auto-install feature in Blender is not supported, you will have to do it manually:

Open the blender/x.x/scripts/addons folder, then pull the io_scene_ac3d folder into the addons folder of blender. There's an alternative location you can drop it, at ~/.blender/x.x/scripts/addons (linux) or c:\Users\[username]\AppData\Roaming\Blender Foundation\Blender\x.x\scrips\addons (Windows 7+), where x.x is the version of Blender and [username] is the Windows user name. Notice AppData per default is hidden in Windows, but you can just write it in the address bar.

## I can't see it in the import/export menu!
You'll need to enable the script in the Blender Preferences window after installing it - open the Blender Preferences window (Edit->Preferences) and then go to the Add-ons tab, select Import-Export in category filter (default value is All) and then check the box on the left of "Import-Export: AC3D (.ac) format"

## Uh, I've done all that how do I use it?
Go to File->Import->AC3D (.ac), select a file, adapt the import settings to your liking, and let it do the work.

## AC3D versions
AC3Db supported for import and export.
AC3Dc supported for import.

## Known Issues:
If exporting when in Edit mode, it will not export the last edits done in Edit mode. Best is to export when in Object mode.

When importing lines, they cannot be assigned UV coordinates as Blender does not support that.

When exporting lines, they will always be smooth shaded, due to limitations in Blender.

When exporting lines they will have the DefaultWhite material, except if their Blender object has only 1 and only 1 material, then they will be assigned that. This is due to Blender limitation.

Exporter will export all materials in object material slots, even if they are not referenced. Good if you had a material you might want to assign to something later. Also annoying cause it potentially can clutter up the AC3D file with unused materials.

## Things to come:
* I want to have an option to overwrite, or to prompt the operator if they want to overwrite textures on an export

## Follow the discussion at:

https://forum.flightgear.org/viewtopic.php?f=18&t=36194

## Complete file format specification, anno 2019

https://sites.google.com/view/ac3dfileformat/home

## Acknowledgments:

The Blender team: (http://www.blender.org) for such a fine piece of software
Willian P Gerano for his original work (the very first version of this script was a port of his original work)
Rene Negree for his help with the importer, tips on the texture mapping and materials and user settings saving
The FlightGear community for their help in testing and feedback for development

- BEGIN GPL LICENSE BLOCK -

  This program is free software; you can redistribute it and/or
  modify it under the terms of the GNU General Public License
  as published by the Free Software Foundation; either version 2
  of the License, or (at your option) any later version.

  This program is distributed in the hope that it will be useful,
  but WITHOUT ANY WARRANTY; without even the implied warranty of
  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
  GNU General Public License for more details.

  You should have received a copy of the GNU General Public License
  along with this program; if not, write to the Free Software Foundation,
  Inc., 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301, USA.

- END GPL LICENSE BLOCK -

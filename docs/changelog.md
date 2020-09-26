##Changelog

###1.4
**2020-09-26**

- Radial Symmetry:
	- New UI showing interactions and controls
	- Added control to show/Hide Pivot
    - Better cancel behaviour

- Rebase Cylinder:
	- Added Ctrl to change Axis
	- Added different merge distance presets
	- Added new Ui 
    - Run on rebased cylinder to change settings
    - Better cancel behaviour

- Quick Lattice:
    - Fix issue with quick lattice vertex group leftovers
    - Fix issue where quick lattice crashes when doing ctrl+z after applying in 2.9
        - Applying lattices now works in 2.9

- Quick Pipe:
	- Control mouse to change segment count
    - Added new Ui
    - Run on spline to change settings
    - Better cancel behaviour

- Smart delete:
	- Added option for toggling between dissolving and removing vertices

- CS Bevel:
    - Fix for 2.9

- Wire/Shaded Toggle:
	- Fixed bug that made the tool not work anymore on some scenes

- Quick Selection
    - Better Grease Pencil Mode
    - Fixed bug when nothing was selected and tool was run

- Transform Mode Cycle:
    - Added Cyclic mode on/off toggle, when off the gizmo is hidden after the scale gizmo

- Smart Modify:
    - Added new options to Object Mode:
        - Object mode:
            -Show / Hide Children
            -Show All

- Transform Options Pie:
    - New pie tool that replaces the old Transform Orientation Pie, snap presets and snap orientation pie
    - Snap Presets Added
    - Proportional Editing Presets Added
    - Transform Pivot Point Added

- Side Menu:
	- Small update for better readability

- Preferences:
	- Added option for smart delete dissolve verts
    - Added Cyclic mode on/off toggle for Transform Mode Cycle. When off the gizmo is hidden after the scale gizmo

- Documentation:
	- New documentation 

- BL Info:
	- Added links to new documentation and bug tracker


###1.3 
**2020-02-20**

- Super Smart Create:
    - Revamped Object Creation Pie:
        - Allows selection between qblocker and normal objects
        - Added camera, light and gpencil and empties

- Quick Pipe:
    - First implementation, makes a quick pipe from the selected edges
    - Mouse left/Right changes size of pipe

- Transform Orientation Pies:
    - Pie menu for pivot orientation, stores 3 custom pivot orientations

- Snap Presets Pie:
    - First Implementation, adds 4 snapping presets that are commonly used while modeling



- Prop Edit Pie:
    - Implemented
    - Control proportional editing settings from this pie.

- Smart Modify Pie:
    - Implemented Tool
    - Context sensitive pie, that brings up relevant tools based on the context.


- Transform:
    - Added CS Move, CS Rotate and CS Scale

- CS Move
    - When executed if you are in a different transform mode it will bring up the respective gizmo.
    - If you are in the move transform mode it will execute the grab tool.
- CS Rotate
    - When executed if you are in a different transform mode it will bring up the respective gizmo.
    - If you are in the move transform mode it will execute the gizmoless rotate tool.

- CS Scale
    - When executed if you are in a different transform mode it will bring up the respective gizmo.
    - If you are in the move transform mode it will execute the resize tool.

- Radial Symmetry:
    - Fixed another Bug that caused the symmetry to be misaligned

- Quick Selection:
    - It now works with Lattices and Grease Pencil objects

- Edit Origin:
    - For version 2.82 and up it now uses the default blender origin edition tool, which supports rotation and does not create an empty
    - If you are in edit mode it will now switch to object mode before editing the origin

- Smart Extrude:
    - A new version of this tool is available. The old version was renamed Smart Extrude Legacy and can be accessed if enabled in the Preferences.
    - The new version uses blender default translation tools, enabling snapping and precise axis control.
    - It remembers what transform tool you were using and executes it after doing the extrude. So it now works with Movement, Rotation and Scale.
    - Contexts work as they used to:
    - If in object mode it will duplicate the object and transform.
    - If in edge selection mode it will extend and transform
    - If in vert or face selection mode it will duplicate and transform
    - If you are in edit mode of a curve, it will extend the curve and transform
    - Setup for executing the tool with shift+drag.

- Side Panel:
    - The SidePanel has been updated with the new tools.

- Smart Extrude Legacy & Smart Translate Legacy:
    - These Tools are now considered Legacy tools and are no longer in development. You can still access them by enabling the legacy tools in the preferences.

- Preferences:
    - Added TexTools integration
    - Added links to recommended addons
    - Added Beta tag to keymap settings section, as its still in development and has bugs atm
    - Add option to enable legacy origin edit mode in versions 2.82 and newer
    - Add Option to Enable Legacy Tools

###1.2.2
**2019-10-20**

- Transform mode cycle:
    - Fixed bug where the tool wouldn’t work if using the Move, Rotate of Scale active tools

- Radial Symmetry

- Option to hide Radial Symmetry pivot

- Quick Lattice:
    - Add Presets to lattice right click menu
    - Option to apply

- Quick Hp Lp Namer:
    - Implemented Tool

- Misc:
    - Added Seams From Islands to the UV Utilities menu for easier access
    - Added entries for the context Menus for Edit Mesh Mode, Object Mode, Uv Mode and Lattice
    - Fixed warnings when loading the plugin

###1.2.1
**2019-10-10**

- Quick Align:
    - Fixed bug where quick align kept the target mesh selected after running

- Quick Lattice:
    - Fixed bug with quick lattice not deleting old lattice vertex groups
    - Fixed bug that didn't allow the lattice to align to the mesh when the tool was run in object mode

- Wire/Shaded toggle:
    - Now remembers what mode was used before switching to wireframe instead of always switching between Solid and wireframe shade mode

- Transform Orientation Cycle:
    - Cycles between the transform orientation modes

- Quick Transform Orientation:
    - If a face, vert or edge is selected it will create a custom transform called “Custom”.
    - If Nothing is selected it will switch to the last used standard orientation.

###1.2
**2019-08-1**

- Super Smart Create:
    - Added partial border detection to fix unexpected results
    - Fixed bug when trying to bridge two faces that were adjacent
- Spline Mode improvements:
    - If in spline/curve mode and nothing selected will execute the spline draw mode
    - If in spline/curve mode and one point is selected it will extrude
    - If in spline/curve mode and 2 open points are selected it will connect them
    - If in spline/curve mode and 2 closed points are selected it will make a point in between
    - Flexi Bezier Tools integration for spline creation,can be enabled/disabled in the preferences
    - Qblocker Integration for object creation mode,can be enabled/disabled in the preferences

- Edit Origin:
    - Fixed bug when you activate the tool from edit mode

- Quick Lattice:
    - Fixed pool method that was filling the console with bug reports

- Smart Modify:

- New Tool that focuses in modifying existing geometry
    - Needs Loop Tools to be enabled to work, with the Edge Flow addon it has extra features
    - If verts are selected it will apply loop tools relax
    - If an open border is selected it will apply loop tools Circle
    - If an edge is selected it will apply set flow, needs the Edge Flow addon
    - If in face mode it will apply loop tools flatten to selected faces

- Quick selection Vert/Edge/Face:
    - Add option to use sticky selection
    - Fixed bug that would make sticky selection not work the first time
    - Removed sticky selection operators as now sticky operation is an option to enable in the preferences menu and they were redundant

- Selection Mode Cycle:
    - Now supports sticky selection if the option is enabled in the preferences menu
    - Fixed a bug when using this tool while selecting a Lattice operator
    - Removed the selection mode cycle sticky operator, as this operator can now replace it

- Seams from hard edges:
    - Only affects selected area, if no selected area is detected then affects everything

- Split UVS by hard edges:
    - Only affects selected area, if no selected area is detected then affects everything

- Preferences Menu:
    - New preferences menu with hotkey setup and preferences for settings for some operators


###1.1 
**2019-07-14**

- General:
    - Updated to work with the 2.8 Release Candidate
    - Code structure was reorganized.
    - New menu structure

- Super Smart Create:
    - Some minor bug fixes
    - Make an edge on a spline
    - Add pie menu to create objects if nothing is selected
    - If at least an object is selected the duplicate pie menu will be called
    - If in vert mode and nothing selected execute the knife tool
    - If in edge mode and no edge selected it will execute the loop cut tool

- Quick Align:
    - Now detects the object that is under the cursor
    - Added option to copy rotation and scale, per axis
    - Has a menu to edit the operation after it has been done

- Smart Loop and Ring:
    - Performance optimization, no longer stalls.

- Quick Origin:
    - Renamed from Quick Pivot to Quick Origin in the menu

- Edit Origin:
    - Renamed from Edit Pivot to Edit Origin in the menu

- Quick Lattice:
    - Quick FFD renamed to Quick Lattice in the menu
    - Fixed bug that prevented lattice to be moved when used on a flat plane

- Rebase Cylinder:
    - Renamed from set cylindrical sides.

- Sticky Selection Vert/Edge/Face:
    - Has been implemented
    - If in object mode it will toggle to edit mode and restore the last selection
    - If in edit mode it will cycle through Vert/Edge/Face modes

- Select mode cycle:
    - Has been implemented
    - If in object mode it will toggle to edit mode
    - If in edit mode it will cycle through Vert/Edge/Face modes

- Smart Delete:

    - If selected verts are only connected to 2 edges it will dissolve them

- Transform mode cycle:
    - Has been implemented
    - It will cycle between Move/Rotate/Scale modes.

    Must be in selection mode for it to work, I will do another version for active tools later.

- Modifiers On/Off:
    - Has been renamed from modifier toggle
    - Now works from edit mode as well

- Seams From Sharps:
    - Applies seams from sharp edges.

- Uvs From Sharps:
    - Applies seams from sharp edges and unwraps everything.
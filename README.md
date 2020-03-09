# TD_Stage_Window

## Features

Create media items and map them onto outputs.



### Shortcuts

Ctrl.1 - Toggle Selection of Cues/Outputs. "Stage Settings/ Selectable Type"

Ctrl.N - Toggle Snapping

Ctrl.D - Duplicate stage items

Hold option / alt while dragging snaps to increments assigned by the user. "Stage Settings/ Translate Increment"

Shift click for multiselection. Multiselect + Middle Button Uniformly scales all items at once.

NOTE: Multiselect does NOT function properly at all with snapping enabled right now.

Backspace - Deletes media items or outputs

# Version History

## 0.06
### User Interface Update
- Classes now have buttons to edit on main comp
- Media Item settings now has a "Stacking Order" page.
  - You have buttons to allow you to change the stacking order of each item.
- Stacking order methods within the Manager class have been updated to function properly.
- Main Comp now has a "New Media Item Expression" parameter. When you create a new piece of media, this expression is assigned to it's top parameter. This way, you can automatically have them select some part of your system, or keep them default.
- Added a "Path To Outputs" parameter on the main Comp. In your build, you'd probably select this comp and handle it as you wish. 
- Added "Selected Media Item Index" parameter to iparStage. You can see this used in Example 1.
- Example 1 is complete - assign your "New Media Item Expression" to automatically select movie engine comp output nulls. Use "Selected Media Item Index to then select the movie engine comp itself, allowing you to control the selected item.
- Buttons added to customize the keyboard shortcuts and drop script.
## 0.04

- Output and media items can now be named
  - Outputs have display labels
  - Note- There's currently a bug with the alpha on these labels so the background may not be transparent.


## 0.03

- Can now snap to center of other objects' either x or y axis.
- Delayed the rendering of lines so they react properly.
- Media Items now have read-only "Computed Resolution" parameters which computes the bounds post scale.

## 0.02
### Snapping Feature Update

- Stage Items save state upon restart.
- Snapping Feature added.
  - Toggle snapping on and off via stage settings or ctrl.n.
  - A line for both X and Y show up when you snap.
  - Snap to any piece of geometry in the scene.
 - As part of the cleanup process, disabling some parameters that are currently not doing anything, but are referenced.
 - Defaul look now has a very dark grid color instead of none.
- Zoom Sensitivity parameter added to stage settings.
## 0.01
### Initial Release


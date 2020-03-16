# TD_Stage_Window

## Description
The Stage Window component provides a workspace to drop "Media Items" or "Output Items" down to freely composite, layout, and map your media to outputs. 

### How does it work?
First, drop an "Output Item" down and a "Media Item" within it's bounds. The output contains a camera that captures anything within it's bounds, so your media will be rendered in place.

### What can you do with it?
It can be used however you see fit. Use it for cropping, scaling, output preview, compositing, or anything a stage layout would be helpful for.  One obvious use case would be splicing up custom resolution media to fit within standard resolutions. 

### How do I get started?
Take a look at the Examples folder, there are some examples of how you might use it. The most important point here is that all you are basically doing is just assigning any top to the top parameter of the "Media Item". There are, of course other features, but that's the general idea.


## Additional Features

Stacking Order



### Shortcuts

Ctrl.1 - Toggle Selection of Cues/Outputs. "Stage Settings/ Selectable Type"

Ctrl.N - Toggle Snapping

Ctrl.D - Duplicate stage items

Hold option / alt while dragging snaps to increments assigned by the user. "Stage Settings/ Translate Increment"

Shift click for multiselection. Multiselect + Middle Button Uniformly scales all items at once.

Ctrl.Shift.Middle Click for non-uniform scale.

NOTE: Multiselect does NOT function properly at all with snapping enabled at the moment. I'll fix it soon.

Backspace - Deletes media items or outputs

# Version History
## 1.01
-Added Render Settings Tab
  - Disable rendering of the main stage
  - Disable preview of outputs


## 1.0
### Cleaned Up and Released

## 0.07
### Callback System
- The Media Items and Output Items now have their own callback dats.
  - Callbacks for both include "OnCreate" and "OnDestroy"
  - Use these to do other things in your program instead of editing the classes
- you can also setup a custom drop script. Example 2 shows drop script functionality

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
- Disabled "Zoom Follows Mouse" because it was terrible. Once I can find a better approach it will come back.
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


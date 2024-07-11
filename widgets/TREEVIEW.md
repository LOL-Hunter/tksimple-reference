# tksimple.TreeView

---
## TreeView-creation
```python
treeview = TreeView(_master, group=None)
```
TODO
tag_configure:
font, image, foreground
## TreeView-Methods
```python
treeview.addEntry(*args, index="end", image=None, tag:str | tuple=None)->None
```
```python
treeview.attachVerticalScrollBar(sc: ScrollBar)->None
```
```python
treeview.clear()->None
```
```python
treeview.clearSelection()->None
```
```python
treeview.createFolder(*args, index="end")->None
```
```python
treeview.deleteItemByIndex(index)->None
```
```python
treeview.getAllSlotIndexes()->None
```
```python
treeview.getAllSlots()->None
```
```python
treeview.getDataByIndex(index)->dict
```
```python
treeview.getIndexByName(item)->None
```
```python
treeview.getSelectedIndex()->None
```
```python
treeview.getSelectedItems()->list
```
```python
treeview.getSize()->None
```
```python
treeview.length()->None
```
```python
treeview.onArrowKeySelectEvent(func, args:list=None, priority:int=0, defaultArgs=False, disableArgs=False, bindToOtherWidget=None)->None
```
```python
treeview.onDoubleSelectEvent(func, args:list=None, priority:int=0, defaultArgs=False, disableArgs=False)->None
```
```python
treeview.onSelectHeader(func, args:list=None, priority:int=0, defaultArgs=False, disableArgs=False, useIndex=False)->None
```
```python
treeview.onSingleSelectEvent(func, args:list=None, priority:int=0, defaultArgs=False, disableArgs=False)->None
```
```python
treeview.see(index)->None
```
```python
treeview.setBgColorByTag(tag:str, color:Color | str)->None
```
```python
treeview.setEntry(*args, index=0)->None
```
```python
treeview.setFgColorByTag(tag:str, color:Color | str)->None
```
```python
treeview.setItemSelectedByIndex(index:int, clearFirst=True)->None
```
```python
treeview.setMultipleSelect()->None
```
```python
treeview.setNoSelectMode()->None
```
```python
treeview.setSingleSelect()->None
```
```python
treeview.setTableHeaders(*args)->None
```
## Widget-Methods
```python
treeview.addChildWidgets(*args)->None
```
Adds/Overwrites all Child widgets from this widget with new ones.
-  args:
- return 
```python
treeview.applyTkOption(**kwargs)->None
```
Apply one or more tkinter attribues to this widget.
Instead of:
widget["text"] = "This is a text!"
Use:
widget.applyTkOption(text="This is a text!", ...)
-  kwargs:
- return 
```python
treeview.attachToolTip(text:str, atext:str="", group=None, waitBeforeShow=.5)->None
```
Attaches a tooltip that opens on hover over this Widget longer than 'waitBeforeShow' seconds.
-  text: Text that will be shown in ToolTip
-  atext: AdditionalText will be shown when shift key is pressed.
-  group: Optional WidgetGroup instance for preset font, color etc.
-  waitBeforeShow: Time the user have to hover over this widget to show the TooTip
- return  ToolTip instance for further configuration
```python
treeview.bind(func:Callable, event:Union[EventType, Key, Mouse, str], args:list=None, priority:int=0, defaultArgs=False, disableArgs=False)->None
```
Binds a specific event to the Widget. Runs given function on trigger.
-  func: function get called on trigger
-  event: Event type: EventType enum or default tkinter event as string.
-  args: Additional arguments as List.
-  priority: If several equal events are bound, it's possible to set priorities.
-  defaultArgs: if True the default tkinter gets passed in bound function instead of Event-instance.
-  disableArgs: if True no args gets passed.
- return 
```python
treeview.canTakeFocusByTab(b:bool=False)->None
```
Set if this widget can take focus by pressing tab.
Default: True
-  b:
- return 
```python
treeview.clearChildWidgets()->None
```
Clears the child-widgets.
- return 
```python
treeview.destroy()->None
```
Destroys this widget.
The Widget instance cannot be used after destroying it!
Can be overwritten!
- return 
```python
treeview.generateEvent(event:Union[EventType, Key, Mouse, str])->None
```
Triggers given event on this widget.
@note Custom Events are not implemented yet!
-  event:
- return 
```python
treeview.getHeight()->None
```
Returns the Widget Height.
May be only possible after using any place manager.
- return 
```python
treeview.getID()->str
```
Returns this widget id.
- return 
```python
treeview.getPosition()->Location2D
```
Returns the widget position.
May be only possible after using any place manager.
- return 
```python
treeview.getPositionToMaster()->Location2D
```
Returns the widget position relative to master window.
May be only possible after using any place manager.
- return 
```python
treeview.getRelScreenPos()->Location2D
```
Returns the location of this widget relative to the screen.
```python
treeview.getText()->None
```
Returns the set text.
- return 
```python
treeview.getTkMaster()->Tk | Toplevel
```
Returns the highest master (Tk/Toplevel) of this widget.
- return 
```python
treeview.getWidth()->None
```
Returns the Widget Width.
May be only possible after using any place manager.
- return 
```python
treeview.grid(row=0, column=0)->None
```
Default tkinter grid-manager.
-  row:
-  column:
- return 
```python
treeview.isFocus()->None
```
Returns a boolean if this widget is currently no focus.
- return 
```python
treeview.lift(widg=None)->None
```
Lifts this widget in front of all other or in front of given Widget.
-  widg:
- return 
```python
treeview.place(x=None, y=None, width=None, height=None, anchor:Anchor=Anchor.UP_LEFT)->None
```
Place the widget with fix coords and width and height.
width and height can be left out and be handled by tkinter to set is automatically.
Can be overwritten!
-  x: X-Coordinate relative to the anchor.
-  y: Y-Coordinate relative to the anchor.
-  width: width of the widget.
-  height: height of the widget.
-  anchor: Set the fixpoint. Default: Upper left corner.
- return 
```python
treeview.placeForget()->None
```
Removes this widget from its master.
Can be placed again after.
- return 
```python
treeview.placeRelative(fixX:int=None,
 fixY:int=None,
 fixWidth:int=None,
 fixHeight:int=None,
 xOffset=0,
 yOffset=0,
 xOffsetLeft=0,
 xOffsetRight=0,
 yOffsetUp=0,
 yOffsetDown=0,
 stickRight=False,
 stickDown=False,
 centerY=False,
 centerX=False,
 changeX=0,
 changeY=0,
 changeWidth=0,
 changeHeight=0,
 nextTo=None,
 updateOnResize=True)->None
```
Scales this widgetsize relative to the Window-Size.
This scaling happens on resize of the window.
Can be overwritten!
Offset:
Offset means to configure the size of the widget percentage to the master size.
xOffsetLeft=50 means that the widget has 50% of the master-width and is right oriented.
-  fixX: Defines x coordinate as fixed. This is no longer autoconfigured.
-  fixY: Defines y coordinate as fixed. This is no longer autoconfigured.
-  fixWidth: Defines width coordinate as fixed. This is no longer autoconfigured.
-  fixHeight: Defines height coordinate as fixed. This is no longer autoconfigured.
-  xOffset: offset x both sides
-  yOffset: offset y both sides
-  xOffsetLeft: offset x left
-  xOffsetRight: offset x right
-  yOffsetUp: offset y up
-  yOffsetDown: offset y down
-  stickRight: Sets the fixpoint to the right side.
-  stickDown: Sets the bottom to the right side.
-  centerY: Centers the widget on Y-Axis.
-  centerX: Centers the widget on X-Axis.
-  changeX: Changes x coordinate after all calculations are done.
-  changeY: Changes y coodinate after all calculations are done.
-  changeWidth: Changes width coodinate after all calculations are done.
-  changeHeight: Changes height coodinate after all calculations are done.
-  nextTo: NOT IMPLEMENTED YET
-  updateOnResize: True -> registers to update on resize (Default) | False -> update once
- return 
```python
treeview.setBg(col:Union[Color, str])->None
```
Set the background color of this widget.
-  col: Use Color enum, tkinter string or hex-code.
- return 
```python
treeview.setBorderWidth(bd:int)->None
```
Some Widgets can change their border size.
-  bd:
- return 
```python
treeview.setCompound(dir_:Direction)->None
```
Select the Compound of an image behind a text.
example:
'Direction.Center' -> centers an image behind a text.
-  dir_:
- return 
```python
treeview.setCursor(c:Cursor)->None
```
Set cursor image from Cursor enum or default tkinter string.
This only applies while hovering over this widget.
@note only predefined cursors are implented yet
-  c:
- return 
```python
treeview.setDisabled()->None
```
Disables this widget.
- return 
```python
treeview.setEnabled()->None
```
Enables this widget.
- return 
```python
treeview.setFg(col:Union[Color, str])->None
```
Set the text color of this widget.
-  col: Use Color enum, tkinter string or hex-code.
- return 
```python
treeview.setFocus()->None
```
Sets the focus to this Window.
- return 
```python
treeview.setFont(size:int=10, art=FontType.ARIAL, underline=False, bold=False, slant=False, overstrike=False)->None
```
Use this method to configure the Font.
-  size: text size
-  art: font type
-  underline: text is underlined
-  bold: text is bold
-  slant: text is slant
-  overstrike: text is overstrike
- return 
```python
treeview.setOrientation(ori:Orient)->None
```
Set the Orientation via Orient enum.
Used for process bars, Scales etc.
Possible orientations:
'Orient.HORIZONTAL'
'Orient.VERTICAL'
-  ori:
- return 
```python
treeview.setStyle(style:Style)->None
```
Set widget style.
Use Style enum to choose between styles.
-  style:
- return 
```python
treeview.setText(text)->None
```
Set the text of this widget.
-  text:
- return 
```python
treeview.setTextOrientation(ori:Anchor=Anchor.LEFT)->None
```
Set the Text align.
Default is 'Anchor.CENTER'
-  ori:
- return 
```python
treeview.unbind(event:Union[EventType, Key, Mouse])->None
```
Unbinds all Events from given EventType.
-  event:
- return 
```python
treeview.unregisterChildWidget(w)->None
```
Unregisters specific Child widget from this Master.
-  w:
- return 
```python
treeview.update()->None
```
Calls the tkinter update of this widget.
Processes all pending Events.
Redaws this widget.
...
- return 
```python
treeview.updateIdleTasks()->None
```
Updates only the tkinter idle tasks.
- return 
```python
treeview.updateRelativePlace()->None
```
Updates the relative place of this widget.
Only updates if the widget ist placed relative.
- return 

# tksimple.SpinBox

---
## SpinBox-creation
```python
spinbox = SpinBox(_master, group=None, optionList:list=(), readOnly=True)
```
## SpinBox-Methods
```python
spinbox.clear()->None
```
```python
spinbox.getValue()->str
```
```python
spinbox.onButtonClick(func, args:list=None, priority:int=0, defaultArgs=False, disableArgs=False)->None
```
```python
spinbox.onUserInputEvent(func, args:list=None, priority:int=0, defaultArgs=False, disableArgs=False)->None
```
```python
spinbox.setButtonBackground(color:Color)->None
```
```python
spinbox.setButtonCursor(cursor:Cursor)->None
```
```python
spinbox.setButtonStyle(style:Style)->None
```
```python
spinbox.setCursorBlinkDelay(d:float)->None
```
```python
spinbox.setCursorColor(c:Color)->None
```
```python
spinbox.setCursorThickness(i:int)->None
```
```python
spinbox.setOptionList(l:list)->None
```
```python
spinbox.setValue(v, clearFirst=True)->None
```
## Widget-Methods
```python
spinbox.addChildWidgets(*args)->None
```
Adds/Overwrites all Child widgets from this widget with new ones.
-  args:
- return 
```python
spinbox.applyTkOption(**kwargs)->None
```
Apply one or more tkinter attribues to this widget.
Instead of:
widget["text"] = "This is a text!"
Use:
widget.applyTkOption(text="This is a text!", ...)
-  kwargs:
- return 
```python
spinbox.attachToolTip(text:str, atext:str="", group=None, waitBeforeShow=.5)->None
```
Attaches a tooltip that opens on hover over this Widget longer than 'waitBeforeShow' seconds.
-  text: Text that will be shown in ToolTip
-  atext: AdditionalText will be shown when shift key is pressed.
-  group: Optional WidgetGroup instance for preset font, color etc.
-  waitBeforeShow: Time the user have to hover over this widget to show the TooTip
- return  ToolTip instance for further configuration
```python
spinbox.bind(func:Callable, event:Union[EventType, Key, Mouse, str], args:list=None, priority:int=0, defaultArgs=False, disableArgs=False)->None
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
spinbox.canTakeFocusByTab(b:bool=False)->None
```
Set if this widget can take focus by pressing tab.
Default: True
-  b:
- return 
```python
spinbox.clearChildWidgets()->None
```
Clears the child-widgets.
- return 
```python
spinbox.destroy()->None
```
Destroys this widget.
The Widget instance cannot be used after destroying it!
Can be overwritten!
- return 
```python
spinbox.generateEvent(event:Union[EventType, Key, Mouse, str])->None
```
Triggers given event on this widget.
@note Custom Events are not implemented yet!
-  event:
- return 
```python
spinbox.getHeight()->None
```
Returns the Widget Height.
May be only possible after using any place manager.
- return 
```python
spinbox.getID()->str
```
Returns this widget id.
- return 
```python
spinbox.getPosition()->Location2D
```
Returns the widget position.
May be only possible after using any place manager.
- return 
```python
spinbox.getPositionToMaster()->Location2D
```
Returns the widget position relative to master window.
May be only possible after using any place manager.
- return 
```python
spinbox.getRelScreenPos()->Location2D
```
Returns the location of this widget relative to the screen.
```python
spinbox.getText()->None
```
Returns the set text.
- return 
```python
spinbox.getTkMaster()->Tk | Toplevel
```
Returns the highest master (Tk/Toplevel) of this widget.
- return 
```python
spinbox.getWidth()->None
```
Returns the Widget Width.
May be only possible after using any place manager.
- return 
```python
spinbox.grid(row=0, column=0)->None
```
Default tkinter grid-manager.
-  row:
-  column:
- return 
```python
spinbox.isFocus()->None
```
Returns a boolean if this widget is currently no focus.
- return 
```python
spinbox.lift(widg=None)->None
```
Lifts this widget in front of all other or in front of given Widget.
-  widg:
- return 
```python
spinbox.place(x=None, y=None, width=None, height=None, anchor:Anchor=Anchor.UP_LEFT)->None
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
spinbox.placeForget()->None
```
Removes this widget from its master.
Can be placed again after.
- return 
```python
spinbox.placeRelative(fixX:int=None,
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
spinbox.setBg(col:Union[Color, str])->None
```
Set the background color of this widget.
-  col: Use Color enum, tkinter string or hex-code.
- return 
```python
spinbox.setBorderWidth(bd:int)->None
```
Some Widgets can change their border size.
-  bd:
- return 
```python
spinbox.setCompound(dir_:Direction)->None
```
Select the Compound of an image behind a text.
example:
'Direction.Center' -> centers an image behind a text.
-  dir_:
- return 
```python
spinbox.setCursor(c:Cursor)->None
```
Set cursor image from Cursor enum or default tkinter string.
This only applies while hovering over this widget.
@note only predefined cursors are implented yet
-  c:
- return 
```python
spinbox.setDisabled()->None
```
Disables this widget.
- return 
```python
spinbox.setEnabled()->None
```
Enables this widget.
- return 
```python
spinbox.setFg(col:Union[Color, str])->None
```
Set the text color of this widget.
-  col: Use Color enum, tkinter string or hex-code.
- return 
```python
spinbox.setFocus()->None
```
Sets the focus to this Window.
- return 
```python
spinbox.setFont(size:int=10, art=FontType.ARIAL, underline=False, bold=False, slant=False, overstrike=False)->None
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
spinbox.setOrientation(ori:Orient)->None
```
Set the Orientation via Orient enum.
Used for process bars, Scales etc.
Possible orientations:
'Orient.HORIZONTAL'
'Orient.VERTICAL'
-  ori:
- return 
```python
spinbox.setStyle(style:Style)->None
```
Set widget style.
Use Style enum to choose between styles.
-  style:
- return 
```python
spinbox.setText(text)->None
```
Set the text of this widget.
-  text:
- return 
```python
spinbox.setTextOrientation(ori:Anchor=Anchor.LEFT)->None
```
Set the Text align.
Default is 'Anchor.CENTER'
-  ori:
- return 
```python
spinbox.unbind(event:Union[EventType, Key, Mouse])->None
```
Unbinds all Events from given EventType.
-  event:
- return 
```python
spinbox.unregisterChildWidget(w)->None
```
Unregisters specific Child widget from this Master.
-  w:
- return 
```python
spinbox.update()->None
```
Calls the tkinter update of this widget.
Processes all pending Events.
Redaws this widget.
...
- return 
```python
spinbox.updateIdleTasks()->None
```
Updates only the tkinter idle tasks.
- return 
```python
spinbox.updateRelativePlace()->None
```
Updates the relative place of this widget.
Only updates if the widget ist placed relative.
- return 

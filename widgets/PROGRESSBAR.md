# tksimple.Progressbar

---
## Progressbar-creation
```python
progressbar = Progressbar(_master, group=None, values:int=100)
```
Widget:
Creates a Processbar to indicate process.
## Progressbar-Methods
```python
progressbar.addValue(v=1)->None
```
Adds a value to the processbar.
Default maxvalue is 100 (full Processbar).
Can be chnged by using 'setValues' method.
-  v:
- return 
```python
progressbar.isFull()->bool
```
Returns a boolean if the Processbar is full.
- return 
```python
progressbar.iter(reset=True)->None
```
A for loop can be used to 'iter' through the processbar.
The for loop index are the steps from the Processbar.
-  reset: if the Processbar should be set to zero before.
- return 
```python
progressbar.reset()->None
```
Sets the bar progress to 0.
Processbar is empty.
- return 
```python
progressbar.setAutomaticMode(delay=0.01)->None
```
Set the Processbar to automatic mode.
The green Bar jumps back and forth.
One cycle takes delay seconds.
-  delay:
- return 
```python
progressbar.setNormalMode()->None
```
Set the Processbar to normal mode.
It can fill from 0 to 100%.
- return 
```python
progressbar.setOrient(o:Orient)->None
```
Set the Processbar orientation using the Orient enum.
Vertical or Horizontal.
-  o:
- return 
```python
progressbar.setPercentage(p:Union[float, int])->None
```
Set Processbar percentage,
Format can be (float) '0.5' -> 50%
Format can be (int) '50' -> 50%
-  p:
- return 
```python
progressbar.setValue(v:int)->None
```
Set the Processbar percentage by value.
Default maxvalue is 100 (full Processbar).
Can be chnged by using 'setValues' method.
-  v:
- return 
```python
progressbar.setValues(val:int)->None
```
Set the max Value.
Value range 0 to 'val'
-  val:
- return 
## Widget-Methods
```python
progressbar.addChildWidgets(*args)->None
```
Adds/Overwrites all Child widgets from this widget with new ones.
-  args:
- return 
```python
progressbar.applyTkOption(**kwargs)->None
```
Apply one or more tkinter attribues to this widget.
Instead of:
widget["text"] = "This is a text!"
Use:
widget.applyTkOption(text="This is a text!", ...)
-  kwargs:
- return 
```python
progressbar.attachToolTip(text:str, atext:str="", group=None, waitBeforeShow=.5)->None
```
Attaches a tooltip that opens on hover over this Widget longer than 'waitBeforeShow' seconds.
-  text: Text that will be shown in ToolTip
-  atext: AdditionalText will be shown when shift key is pressed.
-  group: Optional WidgetGroup instance for preset font, color etc.
-  waitBeforeShow: Time the user have to hover over this widget to show the TooTip
- return  ToolTip instance for further configuration
```python
progressbar.bind(func:Callable, event:Union[EventType, Key, Mouse, str], args:list=None, priority:int=0, defaultArgs=False, disableArgs=False)->None
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
progressbar.canTakeFocusByTab(b:bool=False)->None
```
Set if this widget can take focus by pressing tab.
Default: True
-  b:
- return 
```python
progressbar.clearChildWidgets()->None
```
Clears the child-widgets.
- return 
```python
progressbar.destroy()->None
```
Destroys this widget.
The Widget instance cannot be used after destroying it!
Can be overwritten!
- return 
```python
progressbar.generateEvent(event:Union[EventType, Key, Mouse, str])->None
```
Triggers given event on this widget.
@note Custom Events are not implemented yet!
-  event:
- return 
```python
progressbar.getHeight()->None
```
Returns the Widget Height.
May be only possible after using any place manager.
- return 
```python
progressbar.getID()->str
```
Returns this widget id.
- return 
```python
progressbar.getPosition()->Location2D
```
Returns the widget position.
May be only possible after using any place manager.
- return 
```python
progressbar.getPositionToMaster()->Location2D
```
Returns the widget position relative to master window.
May be only possible after using any place manager.
- return 
```python
progressbar.getRelScreenPos()->Location2D
```
Returns the location of this widget relative to the screen.
```python
progressbar.getText()->None
```
Returns the set text.
- return 
```python
progressbar.getTkMaster()->Tk | Toplevel
```
Returns the highest master (Tk/Toplevel) of this widget.
- return 
```python
progressbar.getWidth()->None
```
Returns the Widget Width.
May be only possible after using any place manager.
- return 
```python
progressbar.grid(row=0, column=0)->None
```
Default tkinter grid-manager.
-  row:
-  column:
- return 
```python
progressbar.isFocus()->None
```
Returns a boolean if this widget is currently no focus.
- return 
```python
progressbar.lift(widg=None)->None
```
Lifts this widget in front of all other or in front of given Widget.
-  widg:
- return 
```python
progressbar.place(x=None, y=None, width=None, height=None, anchor:Anchor=Anchor.UP_LEFT)->None
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
progressbar.placeForget()->None
```
Removes this widget from its master.
Can be placed again after.
- return 
```python
progressbar.placeRelative(fixX:int=None,
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
progressbar.setBg(col:Union[Color, str])->None
```
Set the background color of this widget.
-  col: Use Color enum, tkinter string or hex-code.
- return 
```python
progressbar.setBorderWidth(bd:int)->None
```
Some Widgets can change their border size.
-  bd:
- return 
```python
progressbar.setCompound(dir_:Direction)->None
```
Select the Compound of an image behind a text.
example:
'Direction.Center' -> centers an image behind a text.
-  dir_:
- return 
```python
progressbar.setCursor(c:Cursor)->None
```
Set cursor image from Cursor enum or default tkinter string.
This only applies while hovering over this widget.
@note only predefined cursors are implented yet
-  c:
- return 
```python
progressbar.setDisabled()->None
```
Disables this widget.
- return 
```python
progressbar.setEnabled()->None
```
Enables this widget.
- return 
```python
progressbar.setFg(col:Union[Color, str])->None
```
Set the text color of this widget.
-  col: Use Color enum, tkinter string or hex-code.
- return 
```python
progressbar.setFocus()->None
```
Sets the focus to this Window.
- return 
```python
progressbar.setFont(size:int=10, art=FontType.ARIAL, underline=False, bold=False, slant=False, overstrike=False)->None
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
progressbar.setOrientation(ori:Orient)->None
```
Set the Orientation via Orient enum.
Used for process bars, Scales etc.
Possible orientations:
'Orient.HORIZONTAL'
'Orient.VERTICAL'
-  ori:
- return 
```python
progressbar.setStyle(style:Style)->None
```
Set widget style.
Use Style enum to choose between styles.
-  style:
- return 
```python
progressbar.setText(text)->None
```
Set the text of this widget.
-  text:
- return 
```python
progressbar.setTextOrientation(ori:Anchor=Anchor.LEFT)->None
```
Set the Text align.
Default is 'Anchor.CENTER'
-  ori:
- return 
```python
progressbar.unbind(event:Union[EventType, Key, Mouse])->None
```
Unbinds all Events from given EventType.
-  event:
- return 
```python
progressbar.unregisterChildWidget(w)->None
```
Unregisters specific Child widget from this Master.
-  w:
- return 
```python
progressbar.update()->None
```
Calls the tkinter update of this widget.
Processes all pending Events.
Redaws this widget.
...
- return 
```python
progressbar.updateIdleTasks()->None
```
Updates only the tkinter idle tasks.
- return 
```python
progressbar.updateRelativePlace()->None
```
Updates the relative place of this widget.
Only updates if the widget ist placed relative.
- return 

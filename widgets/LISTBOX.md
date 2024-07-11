# tksimple.Listbox

---
## Listbox-creation
```python
listbox = Listbox(_master, group=None)
```
Widget:
The user can select one (Default) or multiple items.
A Scrollbar can also be added.
## Listbox-Methods
```python
listbox.add(entry:str, index = "end", color:Union[Color, str]=None)->None
```
Adds an entry to the Listbox.
For large amount of items the 'addAll' method is way faster!
-  entry: entry content as string
-  index: where to insert. At the end by default.
-  color: Background color of this item.
- return 
```python
listbox.addAll(entry:[str], index="end", color:Union[Color, str]=None)->None
```
Adds a list of entrys to the Listbox.
When adding large amounts of items this is way faster than 'add' method and a for loop.
-  entry: entry content as string
-  index: where to insert. At the end by default.
-  color: Background color of this item.
- return 
```python
listbox.attachVerticalScrollBar(sc:ScrollBar)->None
```
Used to attach a vertical scrollbar to the Entry.
Pass a Scrollbar instance to this method.
-  sc:
- return 
```python
listbox.bindArrowKeys(widget=None, ifNoSelectionSelect0=True)->None
```
The arrowkeys get bound to navigate up and down via the arrowkeys.
-  widget: bind to given widget (Default = self)
-  ifNoSelectionSelect0: Select on arrowkeys index zero if none is selected
- return 
```python
listbox.clear()->None
```
Removes all items from Listbox.
- return 
```python
listbox.clearSelection()->None
```
Clears the selection.
- return 
```python
listbox.deleteItemByIndex(index:int)->None
```
Deletes an item by given index
-  index:
- return 
```python
listbox.deleteItemByName(name)->None
```
Deletes the first item by given name.
-  name:
- return 
```python
listbox.getAllSlotIndexes()->List[int]
```
Returns a list of indices for every item in Listbox.
- return 
```python
listbox.getAllSlots()->List[str]
```
Returns a list containing all items.
- return 
```python
listbox.getIndexByName(name:str)->None
```
Returns the (first) index by given name.
-  name:
- return 
```python
listbox.getNameByIndex(index:int)->None
```
Returns the name by given index.
-  index:
- return 
```python
listbox.getSelectedIndex()->Union[list, int, None]
```
Returns selected index/indices.
If selectionmode is 'single' -> returns int / None
If selectionmode is 'multiple' -> returns list / None
- return 
```python
listbox.getSelectedItem()->Union[List[str], str, None]
```
Returns selected item/items.
If selectionmode is 'single' -> returns str / None
If selectionmode is 'multiple' -> returns list / None
- return 
```python
listbox.length()->int
```
Returns the amount of items in Listbox.
- return 
```python
listbox.onSelectEvent(func, args:list=None, priority:int=0, defaultArgs=False, disableArgs=False)->None
```
Binds on select event to the Widget. Runs given function on trigger.
-  func: function get called on trigger
-  args: Additional arguments as List.
-  priority: If several equal events are bound, it's possible to set priorities.
-  defaultArgs: if True the default tkinter gets passed in bound function instead of Event-instance.
-  disableArgs: if True no args gets passed.
- return 
```python
listbox.see(index:Union[float, str])->None
```
Adjust the position of the listbox so that the line referred to by index is visible.
'end' for scroll to end.
-  index:
- return 
```python
listbox.setItemSelectedByIndex(index:int, clearFirst=True)->None
```
Set an item selected by given index.
-  index:
-  clearFirst: clears the old selection before setting the new.
- return 
```python
listbox.setItemSelectedByName(name:str, clearFirst=True)->None
```
Set the first item with given name selected.
-  name:
-  clearFirst: clears the old selection before setting the new.
- return 
```python
listbox.setMultipleSelect()->None
```
Set the Listbox in 'multiselectmode'.
The User can select more than one item.
- return 
```python
listbox.setSelectBackGroundColor(c:Union[Color, str])->None
```
Backgroundcolor applied if item is selected.
-  c:
- return 
```python
listbox.setSelectForeGroundColor(c:Union[Color, str])->None
```
Foregroundcolor applied if item is selected.
-  c:
- return 
```python
listbox.setSingleSelect()->None
```
Set the Listbox in 'singleselectmode'.
The User can select only one item.
This is the DEFAULT mode.
- return 
```python
listbox.setSlotBg(index:int, col: Color = Color.WHITE)->None
```
Set backgroundcolor of item a given index.
-  index:
-  col:
- return 
```python
listbox.setSlotBgAll(color:Union[Color, str]=Color.WHITE)->None
```
Set the Backgroundcolor of all slots.
This can be slow.
Better is to set the color while adding.
-  color:
- return 
```python
listbox.setSlotBgDefault(color:Union[Color, str]=Color.WHITE)->None
```
Sets the default color of new added Items.
-  color:
- return 
## Widget-Methods
```python
listbox.addChildWidgets(*args)->None
```
Adds/Overwrites all Child widgets from this widget with new ones.
-  args:
- return 
```python
listbox.applyTkOption(**kwargs)->None
```
Apply one or more tkinter attribues to this widget.
Instead of:
widget["text"] = "This is a text!"
Use:
widget.applyTkOption(text="This is a text!", ...)
-  kwargs:
- return 
```python
listbox.attachToolTip(text:str, atext:str="", group=None, waitBeforeShow=.5)->None
```
Attaches a tooltip that opens on hover over this Widget longer than 'waitBeforeShow' seconds.
-  text: Text that will be shown in ToolTip
-  atext: AdditionalText will be shown when shift key is pressed.
-  group: Optional WidgetGroup instance for preset font, color etc.
-  waitBeforeShow: Time the user have to hover over this widget to show the TooTip
- return  ToolTip instance for further configuration
```python
listbox.bind(func:Callable, event:Union[EventType, Key, Mouse, str], args:list=None, priority:int=0, defaultArgs=False, disableArgs=False)->None
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
listbox.canTakeFocusByTab(b:bool=False)->None
```
Set if this widget can take focus by pressing tab.
Default: True
-  b:
- return 
```python
listbox.clearChildWidgets()->None
```
Clears the child-widgets.
- return 
```python
listbox.destroy()->None
```
Destroys this widget.
The Widget instance cannot be used after destroying it!
Can be overwritten!
- return 
```python
listbox.generateEvent(event:Union[EventType, Key, Mouse, str])->None
```
Triggers given event on this widget.
@note Custom Events are not implemented yet!
-  event:
- return 
```python
listbox.getHeight()->None
```
Returns the Widget Height.
May be only possible after using any place manager.
- return 
```python
listbox.getID()->str
```
Returns this widget id.
- return 
```python
listbox.getPosition()->Location2D
```
Returns the widget position.
May be only possible after using any place manager.
- return 
```python
listbox.getPositionToMaster()->Location2D
```
Returns the widget position relative to master window.
May be only possible after using any place manager.
- return 
```python
listbox.getRelScreenPos()->Location2D
```
Returns the location of this widget relative to the screen.
```python
listbox.getText()->None
```
Returns the set text.
- return 
```python
listbox.getTkMaster()->Tk | Toplevel
```
Returns the highest master (Tk/Toplevel) of this widget.
- return 
```python
listbox.getWidth()->None
```
Returns the Widget Width.
May be only possible after using any place manager.
- return 
```python
listbox.grid(row=0, column=0)->None
```
Default tkinter grid-manager.
-  row:
-  column:
- return 
```python
listbox.isFocus()->None
```
Returns a boolean if this widget is currently no focus.
- return 
```python
listbox.lift(widg=None)->None
```
Lifts this widget in front of all other or in front of given Widget.
-  widg:
- return 
```python
listbox.place(x=None, y=None, width=None, height=None, anchor:Anchor=Anchor.UP_LEFT)->None
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
listbox.placeForget()->None
```
Removes this widget from its master.
Can be placed again after.
- return 
```python
listbox.placeRelative(fixX:int=None,
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
listbox.setBg(col:Union[Color, str])->None
```
Set the background color of this widget.
-  col: Use Color enum, tkinter string or hex-code.
- return 
```python
listbox.setBorderWidth(bd:int)->None
```
Some Widgets can change their border size.
-  bd:
- return 
```python
listbox.setCompound(dir_:Direction)->None
```
Select the Compound of an image behind a text.
example:
'Direction.Center' -> centers an image behind a text.
-  dir_:
- return 
```python
listbox.setCursor(c:Cursor)->None
```
Set cursor image from Cursor enum or default tkinter string.
This only applies while hovering over this widget.
@note only predefined cursors are implented yet
-  c:
- return 
```python
listbox.setDisabled()->None
```
Disables this widget.
- return 
```python
listbox.setEnabled()->None
```
Enables this widget.
- return 
```python
listbox.setFg(col:Union[Color, str])->None
```
Set the text color of this widget.
-  col: Use Color enum, tkinter string or hex-code.
- return 
```python
listbox.setFocus()->None
```
Sets the focus to this Window.
- return 
```python
listbox.setFont(size:int=10, art=FontType.ARIAL, underline=False, bold=False, slant=False, overstrike=False)->None
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
listbox.setOrientation(ori:Orient)->None
```
Set the Orientation via Orient enum.
Used for process bars, Scales etc.
Possible orientations:
'Orient.HORIZONTAL'
'Orient.VERTICAL'
-  ori:
- return 
```python
listbox.setStyle(style:Style)->None
```
Set widget style.
Use Style enum to choose between styles.
-  style:
- return 
```python
listbox.setText(text)->None
```
Set the text of this widget.
-  text:
- return 
```python
listbox.setTextOrientation(ori:Anchor=Anchor.LEFT)->None
```
Set the Text align.
Default is 'Anchor.CENTER'
-  ori:
- return 
```python
listbox.unbind(event:Union[EventType, Key, Mouse])->None
```
Unbinds all Events from given EventType.
-  event:
- return 
```python
listbox.unregisterChildWidget(w)->None
```
Unregisters specific Child widget from this Master.
-  w:
- return 
```python
listbox.update()->None
```
Calls the tkinter update of this widget.
Processes all pending Events.
Redaws this widget.
...
- return 
```python
listbox.updateIdleTasks()->None
```
Updates only the tkinter idle tasks.
- return 
```python
listbox.updateRelativePlace()->None
```
Updates the relative place of this widget.
Only updates if the widget ist placed relative.
- return 

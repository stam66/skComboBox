**Version 0.91**  
Bug fixes for isses:  
- escape not working as intended
- return not working as intended and also setting value when dropdown closed
- not commiting value on clicking out of field
- comboAction transmitting the placeholder text when no value set
  
**Version 0.9**  
- simplified and streamlined
- all code now resides in group script
- All properties have getters/setters
- Simplified getting/setting textContent and listContent
- _comboAction_ message emitted on setting textContent to handle text change
  
  
**Version 0.8**  
A LiveCode group emulating an enhanced combobox replacement:  
Placeholder text function to help guide user input  
Search as you type to highlight a value in the popup  
New values that don’t exist in popup will show an ‘Add’ button to modify popup i  
Remove values in the popup by right-clicking on the value  
Show/hide popup list with the return or escape keys  
Arrow key navigation of popup list  
Select a value in the popup list with the return or enter keys (or click on value)  
Simple API to add list of values for popup and to clear popup.  
A handler skeleton to add action to be triggered after setting a value  
Resize the height/width of the popup list by adjusting the dimensions of the group (make sure 'Select Group' is inactive or group won't resize properly!)  
_**API**_
- _setValueList pValueList_: Populates the popup values with the return-delimited list pValueList. Equivalent to setting the text of a button “ComboBox Menu”. Example: dispatch “setValueList” to group “comboBox” with tValueList  
- _setValue pValue_: Sets the displayed/selected text Equivalent to setting the label of a button “ComboBox Menu”. Example: dispatch “setValue” to group “comboBox" with tValue  
- _setPlaceholderText pText_: Sets the placeholder text to the supplied parameter. Example: dispatch “setPlaceholderText” to group “comboBox” with tText  
- _getPlaceholderText_: Get the placeholder text. Example: send “getPlaceholderText” to group “comboBox —> ‘the result’ now contains the placeholder text  
- _getValue_: Gets the displayed/selected text. Example: send “getValue” to group “comboBox —> ‘the result’ now contains the selected value  
- _getValueList_: Gets the list displayed in the popup (return delimited list). Example: send “getValueList” to group “comboBox —> ‘the result' now contains the selected value  
- _clearCombo_: Clears the popup list and entry field of all values. Example: send “clearCombo” to group “comboBox”  
- _initState_: forces popup closed when card/group containing combobox opens and display either value or the uPlaceholderText correctly. Example: send "initState" to group "comboBox"  

**Version 0.7**
corrected a minor styling issue when first opening the field  
added new command 'initState' - this forces the combobox to not display any values when the card or or group containing this is first openened, and displays correctly value or the uPlaceholderText  
minor change to close popup when value selected  
  
**Version 0.6**  
corrected error with get functions, removed unnecessary custom properties  
added placeholder text functionality  

**Version 0.5**  
fixed get functions corrrectly using 'the result' instead of 'it'  
renamed populateCombo to setValueList for consistency  
added getValueList to get the current list of popup values, as user can modify these  
added doAction handler that triggers when the value of the display field is set, or exited.  

**Version 0.4**  
changed filtering to search-as-you-type to hilight a value in the popup  
if entering text that doesn’t exist in popup, an ‘add’ button will appear to append to popup  
remove values from the popup by right-clicking on the line to remove  
toggle popup with either enter or escape keys  
API modified to avoid direct access of custom property  

How to Make Specific Text Changes in Your TPC1031KT HMI Project
If you want to modify individual labels, buttons, messages, or other displayed text (without setting up full multi-language support), follow these steps:

Method 1: Directly Edit Text in EasyBuilder Pro
Best for: Quick changes to buttons, labels, alarms, etc.

Open Your Project in EasyBuilder Pro.

Select the Object (button, text label, numeric display, etc.) whose text you want to change.

Example: A button that says "START" → Change to "RUN".

Edit the Text Property:

Double-click the object (or check the Property Window).

Find the Text/Caption field and modify it.

If it’s a multi-language object, click ... and edit the text for the active language.

Save & Recompile (F7).

Download to HMI (F5) to apply changes.

Method 2: Bulk Edit Text (Using Excel/CSV Export)
Best for: Changing many labels at once (e.g., translating multiple buttons).

Export Text Entries to CSV:

Go to Tools → Multi-Language Translation Export/Import.

Select Export → Save as .csv.

Edit in Excel:

Open the .csv file in Excel.

Modify the text in the desired language column.

Import Back into EasyBuilder Pro:

Go to Tools → Multi-Language Translation Export/Import → Import.

Select your edited .csv file.

Recompile (F7) and Download (F5).

Common Text Changes & Examples
Object Type	Where to Edit	Example Change
Buttons	Property Window → "Text"	"START" → "RUN"
Labels	Double-click text	"Temperature" → "Temp (°C)"
Alarm Messages	Alarm Manager → Edit Text	"Motor Fault" → "Motor Error"
Numeric Display Units	Property → "Unit Text"	"mm" → "inches"
Troubleshooting
Text Not Updating?

Ensure you recompiled (F7) before downloading.

If using multi-language, verify the correct active language is set.

Special Characters Not Displaying?

Check System Parameters → Font to ensure the font supports your language (e.g., Chinese, Arabic).

Need More Help?
If you want to modify system messages (like date/time format), check System Parameters → Display.

For dynamic text changes (via PLC), you can use String Registers (e.g., LW or RW).
# XPP-TabletAreaConverter
Converts your tablet area from millimeters (mm) to *units* used by XP Pen driver. X and Y offsets are not *yet* supported.

## Method for Conversion

1. Take the active area of the tablet.

   Example: For XP Pen Star G640 it is 6" x 4"

2. Take the full area units of width and height within the XP Pen driver.

   Example: For XP Pen Star G640 the width = 629 and height = 393

3. Convert the active area of the tablet from inches to millimeters.

   ```
   Since: 1 inch = 25.4 millimeters
   
   6 x 25.4 mm = 152.4 mm => width
   4 x 25.4 mm = 101.6 mm => height
   ```

4. Equate the converted units to XP Pen units then get the value of XP Pen units in terms of 1 millimeter.

   ```
   152.4 mm = 629 => width
   101.6 mm = 393 => height
   
   629/152.4 = 4.127296588 => width
   393/101.6 = 3.868110236 => height
   
   Width:	1 mm = 4.127296588 XP Pen units
   Height:	1 mm = 3.868110236 XP Pen units
   ```

5. Set your desired tablet area (in millimeters) through multiplication. The product should be rounded up to a no-decimal number.

   Example: 55.42 mm x 38.19 mm (w x h)

   ```
   55.42 x 4.127296588 = 228.7347769 ~ 229 => width
   38.19 x 3.868110236 = 147.4554991 ~ 148 => height
   ```

6. Put those numbers on the XP Pen driver GUI.

## Requirements
- Functioning tablet
- Windows operating system
- Netframework 4+ (to latest version)

## FAQ

1. How about X-Y Offsets?
   - N/A for now.
2. Only read me for this repo?
   - No, I'm planning to create a simple converter so that I could skip doing these solving.
3. From 2, any ETA?
   - Soon? IDK when I'll start making one, but it should only take about 10-30 minutes.

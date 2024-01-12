# RAD Bot
RAD Bot is a CNC drawing machine powered by Arduino UNO and CNC Shield board and is programmed with GCode/GRBL.
# G Commands Handbook
## G0: Linear Motion (Fast Straight Line)
When you want to start a drawing we recommend that you use G0 to get to your starting point because the pen will move quickly to the point you set. Make sure to set the coordinates of your X and Y end point.
Example:G0 X100 Y100

## G1: Linear Motion (Straight Line)
When you want to draw a line to a different point add your X and Y coordinates after the G1. After the coordinates add the feed rate (F/Speed) and set it to 2000.
Example: G1 X100 Y160 F2000

## G2: Clockwise Arc
This command is ideal for drawing curves, arcs, and circles that are clockwise. How this command works is you set the coordinates that you want to move to. After you set that, add the radius of the circle/arc.
Example: G2 X100 Y100 R50

## G3 Counter Clockwise Arc
This command is ideal for drawing curves, arcs, and circles that are counter clockwise. How this command works is you set the coordinates that you want to move to. After you set that, add the radius of the circle/arc.
Example: G3 X100 Y100 R50

## G92: Save Place
This command is used when you want to set the origin of your machine. After getting to a specific point issue this command like the example shown below. After the G92 command, Make sure to add in the X and Y coordinates after the G92 command.
Example: G92 X0 Y0

# $ Commands Handbook
## $X: Reset
When this command is issued all of your settings will be reset in ChiliPeppr. When you connect your Arduino UNO to your PC you will see a red bar saying alarm state on the right-hand side. Click this to take it out of alarm state.

## $H: Homing Sequence
When this command is issued the X and Y axes will move to the right side of your machine until it engages the contact switches. This tells the machine that this point is the limit. Make sure to set the point as 0,0 after issuing the $H command.

## $$: View Current Arduino Settings
If you issue this command you will be able to see the parameters of the X, Y, and Z axes. You can also view the homing sequence booleans.

# M Commands Handbook
## M3 S90
This command makes the servo motor on the Y-axis turn in its counter clockwise motion for 90 degrees. This causes the pen to go up. If you see that your servo is straining to turn it after it has already completed the turn the timing belt is probably too tight. Make sure to give it some slack.

## M5
This command makes the pen go down after issuing the M3 S90 command to make the pen go up. Make sure, after issuing the command, that the pen is touching the paper after issuing the command of M5.

-The Totally RAD Team

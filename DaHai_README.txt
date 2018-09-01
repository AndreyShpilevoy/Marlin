All my changes are noted with 'DaHai' and a short explaination of the change.

Review these changes against your settings and make the appropriate adjustments before uploading the firmware. There may be (probably are) differences between your Delta setup and mine. 

NOTE: I have TMC2130 on XZY steppers and noted in configuration.h - you probably will need to change those driver types for your printer.

As always, any time you load in new firmware, always use the Control menu to:
1. Initialize EEPROM
2. Restore Failsafe (or Load Factory Setting)
3. Store Settings
And reboot

NOTE: If your printer HOMES in the wrong direction (down instead of up), try reversing the XYZ Directions in configuration.h (even though the Marlin Comment say you can't do that). Change 'false' to 'true' or visa-versa:

// Invert the stepper direction. Change (or reverse the motor connector) if an axis goes the wrong way.
#define INVERT_X_DIR false // DELTA does not invert - DaHai: For TMC2130, you need to reverse the motor connectors
#define INVERT_Y_DIR false
#define INVERT_Z_DIR false
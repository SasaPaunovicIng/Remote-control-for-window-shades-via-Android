# A-OK AC114-01B remote control (RF 433.92MHz) for roller shades and motorized projector screens via Android

A-OK protocol implementation for Arduino and Raspberry Pi. Tested with AM25-1.2/30-MEL-P motors and AC202-02 RF receivers.

https://www.a-okmotors.com/en/

You may find the original code on https://github.com/akirjavainen/A-OK 

Modifications and MIT application done by Saša Paunović.

# How to use
Capture your remote controls with Remote_control_capture.ino and copy&paste the 65 bit commands to Remote_control_roller_shades_via_Android.ino for sendAOKCommand().

More info about this provided in Remote_control_roller_shades_via_Android.ino. 

The Android phone needs to interface with the Arduino over Bluetooth, the App is made to controle 9 shades. 

Play around with the code and make it fit your needs.

# How to use with example commands
  1.  Set the motor or receiver into pairing mode with its PROGRAM button.
  2.  Check the instructions on whether you need to send the pairing command        ("sendAOKCommand(AOK_PROGRAMING);") or UP command ("sendAOKCommand(AOK_UP_#);"). Typically you need to transmit within 10 seconds.
  3.  Now you can control the motor, e.g. "sendAOKCommand(AOK_DOWN_#);" (or AOK_UP_#, AOK_STOP_# etc.).
  
Setting limits for roller shade motors is quicker with the remotes, although you can use your Arduino for that as well.

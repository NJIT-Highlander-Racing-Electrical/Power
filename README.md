# Power

* Zippy 5000mAh 11.1v batteries
  ** Can be ran in parallel after balancing for extra capacity
  ** Housed in a 3D printed dual battery holder
  ** Two thumb screws lock the batteries into place with a cover bar
* 14 AWG wire for main power bus connections
* 24 AWG wire to split off to smaller subsystems 
* Battery Management System
   ** Uses a Low Voltage Disconnect Module to cut off battery power when battery voltage gets too low
   ** BMS can detect low battery to turn on Low Battery LED on dashboard
* CAN-Bus signals are sent over 24 AWG twisted pair wire
* All subsystems use 4-pin Aviation Plug Connectors for 12V power and CAN-Bus signals
* All subsystems will have a 5V switching regulators
   ** Running the vehicle power bus at 12V but each subsystem only requiring 5V allows for a voltage drop on the bus without issues
   ** Switching regulators are far more efficient than linear regulators, which would get too hot stepping down from 12V to 5V at higher loads
   ** The ESP32 can also output 3.3V from the 5V we supply if needed for its subsystems

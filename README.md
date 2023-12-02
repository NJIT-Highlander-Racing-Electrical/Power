# Power
Things to consider are:
* Which battery we are going to use to power all the subsystems (preferably 12V)
  * We can use the Zippy 5000mAh 11.1v batteries
  * If we need a higher capacity, we can run two charged and balanced batteries in parallel
  
* How can we contain these batteries physically and what connectors will we use?

* Can we replace the connectors on the current batteries with XT60 or XT150, and get mating female ones for the vehicle?

* What battery management system we are using

* How we can detect low battery and display it via and LED on the dashboard

* What standardized cables are we using to get 12V to each subsystem
  * Peak estimated power consumption:
      * CVT: 1 amp
      * Dashboard: 2 amp
      * DAQ: 3 amp
      * Steering Angle/Pedals: 1 amp
      * Seat Pressure Mat: 1 amp
      * Total (maximum): 8 amps
  * Using 14 gauge wire should support 10+ Amps
  * We can use 24 gauge wire to split off to smaller subsystems

    
* What standardized cables are we using to send CAN Bus signals throughout the vehicle?

 
* What standardized connectors are we using to disconnect each subsystem
   * 4-pin Aviation Plug Connectors

* How we are stepping down the power from 12V to 5V for each subsystem
  * We can use 5V Voltage Regulators on each subsystem so that each system has a steady 5V, even if the 12V input drops.
  * The ESP32 can also output 3.3V from the 5V we supply if needed for its subsystems

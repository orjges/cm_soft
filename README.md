# cm_soft
Microcontroller-controlled battery cycling and testing mashine. 
Three-phase PWM - controlled charging and discharging of the battery, voltage, current and temperature controlled.

Initial test version: External 2 ADCs (MAX11200) communication and control.
Done:
 - communication over single SPI (2x CS-lines)
 - working mode setup
 - ADC self-calibration (internal offset & gain, external offset*)
 - simultaneous start trigger for both ADCs
 - single-shot sampling

* should be U=0 & I=0 within whole self-calibration cycle

ToDo: 
 - system gain calibration (full scale V & I) (preprocessing within ADC)
 - quadrate-calibration (postprocessing within uC)
 - continuous conversion mode (4x sampling rate vs single-shot)
   + data ready state over GPIO -> interrupt -> get conv. data
   
   

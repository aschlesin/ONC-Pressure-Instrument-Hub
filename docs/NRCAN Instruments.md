### NRCAn Instruments General

These instruments have been deployed at NEPTUNE at various sites, see table below. Their device names in Oceans 3.0 are NRCan Bottom Pressure Recorder XX where XX is the logger ID. There are two different NRCan BPR types:

* Type 1 or ‘TP’, which include a Paroscientific pressure sensor with only a pressure channel and a platinum resistance thermometer or thermistor  
* Type 2 or ‘TTP’, which include a Paroscientific pressure sensor with both pressure and temperature channels and a platinum resistance thermometer or thermistor  
  * Some ‘TTP’ BPRs are referred as ‘TTP-minusT’, as they do not contain a platinum thermistor sensor

These BPRs use Paroscientific pressure sensors model 8B4000-1 or 8B4000-2. Model naming breakdown:

* 8B: Series 8B "High Pressure Absolute Depth Sensors"  
* 4000: max depth in metres  
* \-1: single output, pressure only  
* \-2: pressure and temperature output

Are Paroscientific model 4000KR also used? I could not find records in Jira of this model being used.

## Sensor Naming Conventions (e.g., what does SCVIPBPR mean?)

Sensors are dependent on the type of BPR, as follows.

* NRCan Sensor Naming Scheme in Oceans3.0:  
  * DART Pressure Residual: contains raw pressure readings that have their tidal portion removed to leave only noise and pressure spikes.  
  * Housing Temperature: corresponds to the readings from the  platinum sensor inside the housing. However, it is tightly coupled with the water temperature even though it is not in-situ.  
  * Instrument Clock: measures the BPR internal clock.  
  * P-Sensor Temperature: Reported only for **TTP** type. It corresponds to the temperature measurements from the Paroscientific pressure sensor. These readings are used to calibrate the pressure measurements which are reported by the Seafloor Pressure sensor.  
  * Seafloor Pressure: readings are dependent on the BPR type as follows:  
    * For **TP** type, pressure values are calibrated using the Housing Temperature readings which influence (falsify) the Pressure readings for short-term events due to the Housing Temperature being noise sensitive to small environmental changes.  
    * For **TTP** and **TTP-minusT** types, pressure values are calibrated using the Paroscientific internal temperature readings, which are less noise sensitive to small environmental changes compared to those of the TP type.  
  * Uncompensated Seafloor Pressure: these sensors are only present in the **TP** type, as TTP devices have internal temperature sensors to compensate/calibrate the pressure readings, which have the same level of sensitivity as the pressure sensors and do not falsify the readings. For the **TP** type, these sensor readings enable a better evaluation of these short-term events, as they are not influenced by the Housing Temperature calibration. 


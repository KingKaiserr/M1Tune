//## Dyno Prep - Logging, MAP, Idle Actuator  

**Date:** April 13, 2026  
**Author:** Ananya  

Coolant Temperature Sensor Voltage Reference: Sensor 5 0V A -> Sensor 5 0V B  Controls which 5V supply rail the coolant temp sensor normalizes against. Changed to match the correct rail for Analogue Temperature Input 2 per harness doc.  

Logging Delay: 30.0s -> 0.1s  Delay before logging starts. Reduced to capture data from engine startup.  

Logging Throttle Pedal: 60.0% -> 0.0%  Throttle position threshold required to trigger logging. Reduced to 0 so logging captures idle and low load data.  

Logging Engine Speed: 0.0 rpm -> 500.0 rpm  Engine speed threshold to trigger logging. Set to 500 rpm so logging starts automatically when engine fires.  

Brake Switch Threshold: 0.0V -> 2.0V  Voltage threshold for brake switch input. Set to standard switch threshold value to clear invalid configuration.  

Brake Switch Hysteresis: 0.0V -> 0.5V  Hysteresis band for brake switch. Set to standard value to clear invalid configuration.  

Driver Switch 3 Threshold: 0.0V -> 2.0V  Voltage threshold for shutdown trigger input on E2.14. Set to standard switch threshold value.  

Driver Switch 3 Hysteresis: 0.0V -> 0.5V  Hysteresis band for Driver Switch 3. Set to standard value.  

Driver Switches 4-8 Threshold: 0.0V -> 2.0V  Voltage thresholds for unconnected driver switch inputs. Set to clear invalid configuration.  

Driver Switches 4-8 Hysteresis: 0.0V -> 0.5V  Hysteresis bands for unconnected driver switch inputs. Set to clear invalid configuration.  

Engine Oil Pressure Low Switch Threshold: 0.0V -> 2.0V  Voltage threshold for oil pressure switch input. Set to clear invalid configuration.  

Engine Oil Pressure Low Switch Hysteresis: 0.0V -> 0.5V  Hysteresis band for oil pressure switch. Set to clear invalid configuration.  

Idle Switch Threshold: 0.0V -> 2.0V  Voltage threshold for idle switch input. Set to clear invalid configuration.  

Idle Switch Hysteresis: 0.0V -> 0.5V  Hysteresis band for idle switch. Set to clear invalid configuration.  

Steering Pressure Switch Threshold: 0.0V -> 2.0V  Voltage threshold for steering pressure switch input. Set to clear invalid configuration.  

Steering Pressure Switch Hysteresis: 0.0V -> 0.5V  Hysteresis band for steering pressure switch. Set to clear invalid configuration.  

Idle Mass Flow Proportional Gain: 0.0 %/10... -> 0.5 %/10...  Proportional gain for idle mass flow control loop. Changed from zero to provide proportional response — running pure integral with no proportional caused slow hunting behavior.
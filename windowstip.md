List of all devices that support waking the computer from any sleep state.
     powercfg -devicequery wake_from_any

Allow Device to Wake the Computer
     powercfg -deviceenablewake "{Device_Name}"

List of all devices that are able to wake the computer. 
     powercfg -devicequery wake_armed

Prevent Device from Wakeing the Computer
     powercfg -devicedisablewake "{Device_Name}"
 

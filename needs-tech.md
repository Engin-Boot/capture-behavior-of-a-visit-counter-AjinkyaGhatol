# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given system stores data on multiple servers
  When system restarts
  Then recover data from nearest server available
  
Scenario: Reconcile counts if the sensor is offline for a while

  Given hospital has installed number of sensors and at least
  one of them is online at any time
  When any one of the sensor goes offline
  Then visitor enters through another available sensor gate
  note: Hospital uses card reader sensor and each user gets card
  at main gate of hospital area
  
Scenario: Director wants report of custom time period

  Given: Syatem stores live data on server with corresponding timespam
  When director press generate report button on user interface
  Then system fetch data between given time period from nearest server
  and generates report wich provides graphical representation of data
  
Scenario: Electric power source from mincipal corporation break

  Given: Hospital has installed generators and system has its own power source
  When system identifies break in power source
  Then it turns on generator of hospital

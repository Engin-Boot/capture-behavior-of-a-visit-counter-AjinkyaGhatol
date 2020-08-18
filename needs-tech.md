# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given system stores data on multiple servers
  When system restarts
  Then recover data from nearest server available

Scenario: Reconcile counts if the sensor is offline for a while

  Given hospital has installed many number of sensors and at least
  one of them is online at any time
  When any one of the sensor goes offline
  Then visitor enters through another available sensor gate
  note: Hospital uses card reader sensor and each user gets card
  at main gate of hospital area

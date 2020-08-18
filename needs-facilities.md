# Visit-counter for a Facilities Manager

note: hospital has two parking areas: one in open ground or area and second in
basement of hospital where basememt parking is reserved for staff and specialist
of hospital. 

Scenario: Parking slot in open ground available and visitor is other than staff of
hospital
  
  Given parking management system in hospital shows live number of parking
  slots available to the staff at entry gate of hospital and slot is available
  for parking
  When visitor visits with car or bike
  Then parking management staff books one of parking slot for the visitor in
  parking management system and decrements the count of available parking slot
  and lights in parking area  guides the visitor to location of parking slot.
  
Scenario: Parking slot not available in open ground and visitor is other than staff of
hospital and not a patient
  
  Given parking management system in hospital shows live number of parking slots
  available to the staff at entry gate of hospital and slot is not available for
  parking
  When visitor visits with car or bike
  Then visitor parks the vehicle outside of hospital area.
  
Scenario: Parking slot not available in open ground and visitor is other than staff of
hospital and is a patient

  Given parking management system in hospital shows live number of parking slots
  available to the staff at entry gate of hospital and slot is not available for
  parking in open area and slot is available in basement
  When visitor visits with car or bike
  Then staff at entry gate books one parking slot for the patient in hospitals
  basement parking and lights in parking area  guides the visitor to location of
  parking slot.

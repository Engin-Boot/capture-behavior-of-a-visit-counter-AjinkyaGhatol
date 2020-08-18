# Visit-counter for a Director

note: Hospital has storage area which maintains stock for extra beds.

Scenario: Only 10 percent of beds are remaining out of all beds

  Given management system in hospital sent report about number of beds to
  director
  When Director got the report
  Then Director ordered staff to bring 40 percentage of current beds from the
  storage area of hospital 

Scenario: Only 10 percent of nursing staff are remaining out of all nursing
staff

  Given management system in hospital sent report about number of beds to
  director
  When Director got the report
  Then Director contacted hospital nearby for availability of nurses and hire
  nursing staff for his hospital

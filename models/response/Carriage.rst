====
Carriage
====

#.  bool **ereg_is_available** Is available electronic registration for this carriage;

#.  string **carriage_number** Number of carriage;

#.  int **bottom_compartment_places** Quantity of places;

#.  int **top_compartment_places** Quantity of places;

#.  int **bottom_side_places** Quantity of places. This type of places exist only in 3rd class;

#.  int **top_side_places** Quantity of places. This type of places exist only in 3rd class;

#.  int **whole_compartments** Quantity of whole compartments;

#.  string **free_place_numbers** Numbers of available places;

#.  `GenderDependentAvailability <GenderDependentAvailability.rst>`_ **gender_dependent_availability** For carriages with male/female service this property will contain gender dependent availability;

#.  bool **is_gender_dependent** Is carriage a gender dependent. If this property is true then "genderDependentAvailability" should be parsed. To buying ticket into this carriage `BookTickets.Selection.cabin_gender_type <../request/Selection.rst>`_ should be specified;


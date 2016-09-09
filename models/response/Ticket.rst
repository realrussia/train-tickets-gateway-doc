====
Ticket
====

#.  int **ticket_id** Identifier of permanent ticket;

#.  int **registration_type** Registration type Id;

#.  int **status** Ticket status Id;

#.  string **place_number** Number of places. Can contain few places;

#.  `Price <Price.rst>`_ **price** Price amounts;

#.  string **booking_date** Date of booking;

#.  string **cancellation_date** Date of cancellation. If ticket not cancelled field will be empty;

#.  `Person <Person.rst>`_\[] **passengers** Passengers information;

#.  string **change_meal_before** You can change the meal (if it's provided) before the time. Format ISO 8601 ('YYYY-MM-DDThh:mm:ss±hh:mm'). Example: 2015-12-16T20:17:00+03:00;

#.  `Meal <Meal.rst>`_ **meal**;


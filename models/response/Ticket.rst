====
Ticket
====

My short description

Full description here

#.  int **ticketId** Identifier of permanent ticket;

#.  int **registrationType** Registration type Id;

#.  int **status** Ticket status Id;

#.  string **placeNumber** Number of places. Can contain few places;

#.  `Price <Price.rst>`_ **price** Price amounts;

#.  string **bookingDate** Date of booking;

#.  string **cancellationDate** Date of cancellation. If ticket not cancelled field will be empty;

#.  `Person <Person.rst>`_\[] **passengers** Passengers information;

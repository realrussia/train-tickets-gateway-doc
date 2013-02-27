#Ticket

 My short description

 Full description here

 1.  int **ticketId** Identifier of permanent ticket;

 1.  int **registrationType** Registration type Id;

 1.  int **status** Ticket status Id;

 1.  string **placeNumber** Number of places. Can contain few places;

 1.  [Price](Price.rst) **price** Price amounts;

 1.  string **bookingDate** Date of booking;

 1.  string **cancellationDate** Date of cancellation. If ticket not cancelled field will be empty;

 1.  [Person](Person.rst)[] **passengers** Passengers information;

====
BookTickets
====

#.  int **st1** Departure station Id;

#.  int **st2** Arrival station Id;

#.  string **dt** Departure date;

#.  string **train_number** Train number has to be `transliterated </articles/trainNumbers.rst>`_ .To avoid problems need to send train number specified in `ServiceClass </models/response/ServiceClass.rst>`_ if it is set;

#.  int **carriage_class_id**;

#.  `Selection <Selection.rst>`_ **selection**;

#.  `Ticket <Ticket.rst>`_\[] **tickets**;

#.  `Delivery <Delivery.rst>`_ **delivery**;

#.  int **id** Not required;


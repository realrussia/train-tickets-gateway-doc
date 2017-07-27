====
BookTickets
====

#.  int **st1** Departure station Id;

#.  int **st2** Arrival station Id;

#.  string **dt** Departure date;

#.  string **departure_time** Departure time in format 'hh:mm'. For russian stations time should be in the moscow timezone.
    For stations of other countries time should in the local timezone.
    Note, this parameter can be omitted, but we can't guarantee successful booking without it.;

#.  string **train_number** Train number has to be `transliterated </articles/trainNumbers.rst>`_ .To avoid problems need to send train number specified in `ServiceClass </models/response/ServiceClass.rst>`_ if it is set;

#.  int **carriage_class_id**;

#.  `Selection <Selection.rst>`_ **selection**;

#.  `Ticket <Ticket.rst>`_\[] **tickets**;

#.  `Delivery <Delivery.rst>`_ **delivery**;

#.  int **id** Not required;


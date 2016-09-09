====
Order
====

#.  string **reference_number**;

#.  int **booking_transaction_id**;

#.  int **cancellation_transaction_id**;

#.  `TrainShort <TrainShort.rst>`_ **train**;

#.  float **price**;

#.  int **carriage_class** Carriage class Id;

#.  string **services** Services Ids divided by ",";

#.  string **carriage_number**;

#.  `Ticket <Ticket.rst>`_\[] **tickets**;


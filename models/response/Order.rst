====
Order
====

#.  string **referenceNumber**;

#.  int **bookingTransactionId**;

#.  `Train <Train.rst>`_ **train**;

#.  float **price**;

#.  int **carriageClass** Carriage class Id;

#.  string **services** Services Ids divided by ",";

#.  string **carriageNumber**;

#.  `Ticket <Ticket.rst>`_\[] **tickets**;

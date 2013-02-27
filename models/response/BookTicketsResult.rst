====
BookTicketsResult
====

Temporary booking order. It will be removed after confirmation or declination

#.  int **preOrderId** Id of temporary booking order;

#.  `Train <Train.rst>`_ **train**;

#.  string **buyingTime** Time of request;

#.  string **carriageNumber**;

#.  int **carriageClassId**;

#.  int **cabinGenderType**;

#.  int **placesCount**;

#.  float **price**;

#.  `BookingCacheTicket <BookingCacheTicket.rst>`_\[] **tickets**;

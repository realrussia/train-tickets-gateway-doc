====
BookTicketsResult
====

Temporary booking order. It will be removed after confirmation or declination

#.  int **pre_order_id** Id of temporary booking order;

#.  `Train <Train.rst>`_ **train**;

#.  string **buying_time** Time of request;

#.  string **carriage_number**;

#.  int **carriage_class_id**;

#.  int **cabin_gender_type**;

#.  int **places_count**;

#.  float **price**;

#.  `BookingCacheTicket <BookingCacheTicket.rst>`_\[] **tickets**;

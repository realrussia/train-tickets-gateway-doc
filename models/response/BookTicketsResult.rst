====
BookTicketsResult
====

#.  int **pre_order_id** Id of temporary booking order;

#.  `Train <Train.rst>`_ **train**;

#.  string **buying_time** Time of request;

#.  string **carriage_number**;

#.  int **carriage_class_id**;

#.  string **carriage_owner**;

#.  int **cabin_gender_type**;

#.  int **places_count**;

#.  float **price**;

#.  `BookingCacheTicket <BookingCacheTicket.rst>`_\[] **tickets**;

#.  int **request_id** ID of request specified in `BookTickets <Input/BookTickets.rst>`_;

#.  bool **is_print_point_at_departure_station_available** Is print point for Etickets available on the station of departure;


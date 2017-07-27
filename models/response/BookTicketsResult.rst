====
BookTicketsResult
====

    Temporary booking order. It will be removed after confirmation or declination

#.  int **pre_order_id** Id of temporary booking order;

#.  int **order_id** Id of booking order
    For the manual issue solve;

#.  `Train <Train.rst>`_ **train**;

#.  string **buying_time** Time of request;

#.  string **carriage_number**;

#.  int **carriage_class_id**;

#.  string **ufs_service_class_code**;

#.  string **carriage_owner**;

#.  int **cabin_gender_type**;

#.  int **places_count**;

#.  float **price**;

#.  `BookingCacheTicket <BookingCacheTicket.rst>`_\[] **tickets**;

#.  int **request_id** ID of request specified in `BookTickets <Input/BookTickets.rst>`_;

#.  bool **is_print_point_at_departure_station_available** Is print point for Etickets available on the station of departure;

#.  string **notification_message** Notification message with additional information;

#.  string **time_information** Information about timezones of arrival and departure stations;


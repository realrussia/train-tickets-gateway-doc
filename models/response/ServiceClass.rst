====
ServiceClass
====

#.  int **carriage_class_id**;

#.  string **carriage_class_code**;

#.  string **rzhd_service_class_id**;

#.  string **services**;

#.  string\[] **service_tags**;

#.  string **train_thread_number** Some service classes can have different train number than whole `Train </models/response/Train.rst>`_ . You should specify this train number to book tickets in this service class. Example of this you can see on the train 055 from Moscow(8631) to Orsha(9778). Train number is `transliterated </articles/trainNumbers.rst>`_;

#.  `CarriageOwner <CarriageOwner.rst>`_ **carriage_owner**;

#.  `Carriage <Carriage.rst>`_\[] **carriages**;

#.  `SeatsAvailability <SeatsAvailability.rst>`_\[] **seats_availability**;

#.  int **cost_for_two_places** 1 - true. 0 - false;

#.  int **cost_for_four_places** 1 - true. 0 - false;

#.  float **price** NOTE: this is approximate price, accurate price will be shown only in `TicketsController.bookTickets </controllers/TicketsController.rst#booktickets>`_;

#.  float **min_price** NOTE: this is approximate price, accurate price will be shown only in `TicketsController.bookTickets </controllers/TicketsController.rst#booktickets>`_
Probably this is price for low seats;

#.  float **min_price_for_child** NOTE: this is approximate price, accurate price will be shown only in `TicketsController.bookTickets </controllers/TicketsController.rst#booktickets>`_
Probably this is price for low seats;

#.  float **price_for_child** This tag is optional. It will be shown only for `InformationController.getTrain </controllers/InformationController.rst#gettrain>`_. NOTE: this is approximate price, accurate price will be shown only in `TicketsController.bookTickets </controllers/TicketsController.rst#booktickets>`_;

#.  int **places_per_cabin** Number of places in cabin. If there is no cabins in such type of carriage then this tag will contain 0;

#.  int **is_two_storey** 1 - true. 0 - false;

#.  float **cost** Maximum RZHD cost of tickets in the service class;

#.  float **min_cost** Minimal RZHD cost of tickets in the service class;

#.  string **international_service_class** International service class. Can be specified for some international trains.
It should be sent with booking request in `ServiceClass </models/response/ServiceClass.rst>`_;

#.  bool **is_the_whole_coupe_booking_available** Availability to book a whole coupe. At the beginning of September 16 the feature available only on Moscow - Riga route.;


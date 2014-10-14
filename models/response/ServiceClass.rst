====
ServiceClass
====

#.  int **carriage_class_id**;

#.  string **rzhd_service_class_id**;

#.  string **services**;

#.  string **train_thread_number** Some service classes can have different train number than whole `Train </models/response/Train.rst>`_ . You should specify this train number to book tickets in this service class. Example of this you can see on the train 055 from Moscow(8631) to Orsha(9778). Train number is `transliterated </articles/trainNumbers.rst>`_;

#.  `Carriage <Carriage.rst>`_\[] **carriages**;

#.  `SeatsAvailability <SeatsAvailability.rst>`_\[] **seats_availability**;

#.  int **cost_for_two_places** 1 - true. 0 - false;

#.  float **price** NOTE: this is approximate price, accurate price will be shown only in `TicketsController.bookTickets </controllers/TicketsController.rst#booktickets>`_;

#.  float **price_for_child** This tag is optional. It will be shown only for `InformationController.getTrain </controllers/InformationController.rst#gettrain>`_. NOTE: this is approximate price, accurate price will be shown only in `TicketsController.bookTickets </controllers/TicketsController.rst#booktickets>`_;

#.  int **places_per_cabin** Number of places in cabin. If there is no cabins in such type of carriage then this tag will contain 0;


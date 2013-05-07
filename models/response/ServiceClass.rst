====
ServiceClass
====

#.  int **carriage_class_id**;

#.  string **services**;

#.  `Carriage <Carriage.rst>`_\[] **carriages**;

#.  `SeatsAvailability <SeatsAvailability.rst>`_\[] **seats_availability**;

#.  int **cost_for_two_places** 1 - true. 0 - false;

#.  float **price** NOTE: this is approximate price, accurate price will be shown only in `TicketsController.bookTickets </controllers/TicketsController.rst#booktickets>`_;

#.  float **price_for_child** This tag is optional. It will be shown only for `InformationController.getTrain </controllers/InformationController.rst#gettrain>`_. NOTE: this is approximate price, accurate price will be shown only in `TicketsController.bookTickets </controllers/TicketsController.rst#booktickets>`_;


====
Selection
====

#.  string **carriage_number**;

#.  string **places_range** Range in format ``/\d(-\d)?/``. Not required tag;

#.  int **registration_type** Not required tag. Default value = 2;

#.  int **tier** Not required tag. Default value = 1;

#.  int **cabin_gender_type** Not required tag. Default value = 1;

#.  int **in_one_kupe** *Kupe* means Coupe. If 1 set then system will book tickets only in one compartment. Not required tag. Default value = 1. For "Seat only" carriage class it will be forced to 0.;

#.  string **rzhd_service_class_id** This parameter is not required at the moment but Rzhd possibly can make it a required in future. Parameter can be required in some specific cases.
    For example: if there is more than one type of service in the same carriage.
    Example: Trains with numbers greater than 800 from Moscow to Ryazan, Kaluga, Saint-Petersburg etc.
    Value for this parameter should be gotten from `InformationController.getTrain() </controllers/InformationController.rst#gettrain>`_ `Train.ServiceClass.rzhd_service_class_id <../response/ServiceClass.rst>`_ as it is;

#.  bool **are_places_with_pets_required** Not required. Specified for automatic booking of places for passengers with pets;

#.  int **storey** The parameter is required for double deck carriages;

#.  int **additional_requirements**;

#.  string **international_service_class** International service class.
    Value for this parameter should be gotten from `InformationController.getTrain() </controllers/InformationController.rst#gettrain>`_
    `Train.ServiceClass.international_service_class <../response/ServiceClass.rst>`_ as it is;

#.  bool **book_the_whole_coupe** Not required tag. Allows to book a whole coupe if the feature available in the service class
    `Train.ServiceClass.is_the_whole_coupe_booking_available <../response/ServiceClass.rst>`_;


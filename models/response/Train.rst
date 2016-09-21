====
Train
====

    Extends from `TrainShort <./TrainShort.rst>`_ in some responses

#.  `Station <Station.rst>`_ **station1** Translated station name;

#.  `Station <Station.rst>`_ **station2** Translated station name;

#.  int **running_time**;

#.  int **distance**;

#.  string **train_number_for_user** Sometimes the train number can be changed a little bit after purchasing. This field stores an alternative number;

#.  string **train_name**;

#.  bool **ereg_is_available**;

#.  string **services**;

#.  `ServiceClass <ServiceClass.rst>`_\[] **service_classes**;

#.  string\[] **countries_of_visit**;

#.  bool **is_er_expiration_day** A train is en route or departs during the day.;

#.  string **allowed_document_types**;

#.  int **station1_id**;

#.  int **station2_id**;

#.  string **departure_date_time** Format ISO 8601 ('YYYY-MM-DDThh:mm:ss±hh:mm'). Example: 2015-12-16T20:17:00+03:00;

#.  string **arrival_date_time** Format ISO 8601 ('YYYY-MM-DDThh:mm:ss±hh:mm'). Example: 2015-12-16T20:17:00+03:00;

#.  string **train_number** Train number is `transliterated </articles/trainNumbers.rst>`_;


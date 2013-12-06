====
Person
====

#.  string **name**;

#.  string **middle_name**;

#.  string **surname**;

#.  string **birth_date** This field is required;

#.  int **sex** 0 - female, 1 - male. This field is required;

#.  string **citizenship** Citizenship in format ISO 3166-1 alpha-2. Look at the `ReferenceController.countries() </controllers/ReferenceController.rst#countries>`_;

#.  `Document <Document.rst>`_ **document**;

#.  int **tariff** ID of tariff;

#.  string **country_of_birth** Country of birth in format ISO 3166-1 alpha-2. Look at the `ReferenceController.countries() </controllers/ReferenceController.rst#countries>`_ . This field is required;


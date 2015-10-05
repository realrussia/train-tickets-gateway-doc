====
Person
====

#.  string **name** Length <= 20 characters;

#.  string **middle_name** Length <= 20 characters;

#.  string **surname** length(name) + length(middle_name) + length(surname) < 70 characters;

#.  string **birth_date** This field is required;

#.  int **sex** 0 - female, 1 - male. This field is required;

#.  string **citizenship** Citizenship in format ISO 3166-1 alpha-2. Look at the `ReferenceController.countries() </controllers/ReferenceController.rst#countries>`_;

#.  `Document <Document.rst>`_ **document**;

#.  int **tariff** ID of tariff;

#.  string **country_of_birth** Deprecated! Alias for PlaceOfBirth. Will be removed soon;

#.  string **place_of_birth** Deprecated! Will be removed soon;


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

#.  string **country_of_birth** Deprecated! Alias for PlaceOfBirth. Will be removed soon;

#.  string **place_of_birth** Place of birth that specified in document. If there is no such field than should be sent "-". Value should be less than 99 symbols. Allowed latin, cyrillic symbols, digits, commas, dashes and spaces;


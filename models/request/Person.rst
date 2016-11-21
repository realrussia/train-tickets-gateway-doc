====
Person
====

#.  string **name** Length <= 20 characters;

#.  string **middle_name** Length <= 20 characters;

#.  string **surname** length(name) + length(middle_name) + length(surname) < 70 characters;

#.  string **birth_date** This field is required;

#.  int **sex** 0 - female, 1 - male. This field is required;

#.  string **country_of_document** Country of document in format ISO 3166-1 alpha-2. Look at the `ReferenceController.countries() </controllers/ReferenceController.rst#countries>`_;

#.  `Document <Document.rst>`_ **document**;

#.  int **tariff** `Tariff ID <../../../controllers/ReferenceController.rst#tariffs>`_;

#.  string **citizenship** Will be removed soon. Use field "country_of_document" instead;

#.  string **country_of_birth** Deprecated! Alias for PlaceOfBirth. Will be removed soon;

#.  string **place_of_birth** Deprecated! Will be removed soon;


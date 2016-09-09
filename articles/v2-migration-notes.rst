====
Migration notes for v2
====

Look breakingchanges_.

.. _breakingchanges:
Breaking changes
====

response/Train
  * Times of departure and arrival are changed the format to ISO 8601 ('YYYY-MM-DDThh:mm:ss±hh:mm')

.. _deprecations:
Deprecations
====

request/Person
  * *citizenship* is softly renamed to *country_of_document* because it more semantically suitable to RZHD requirements

.. _amends:
Amends
====

.. _amendscontrollers:
Controllers
----

FilesController
 * Into *getEticket* added a possibility to get file by ticket's ID. New parameter *search_by* helps
 * New method *getCancellationForm* added to make possible to receive the file

InformationController
 * New method *getRoute*
 * New method *getAvailableMeals*. Allows to fetch list of available meals that can be used for `changeMeal </controllers/TicketsController.rst#changemeal>`_

ReferenceController
 * `documentTypes </controllers/ReferenceController.rst#documenttypes>`_ now has a format's description
 * New methods added `additionPlacesRequirements </controllers/ReferenceController.rst#additionplacesrequirements>`_

TicketsController
 * New method `bookPackage </controllers/TicketsController.rst#bookpackage>`_ allows to book few tickets at once.
 * New method `changeMeal </controllers/TicketsController.rst#changemeal>`_ allows to change meal for `Ticket </models/response/Ticket.rst>`_ : meal (if it's provided)

.. _amendsmodels:
Models
----

request/Selection
 * Few new properties added

response/Carriage
 * Added availability of few new types of places

response/ServiceClass
 * Added information about carriage owner, service tags and few other carriage options

response/Train
 * Added information about distance, stations translation, countries of visit and allowed document types

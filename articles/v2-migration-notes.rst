====
Migration notes for v2 
====

* `Breaking changes <#breaking-changes>`_
* `Deprecations <#deprecations>`_
* `Amends <#amends>`_
 * `Controllers <#controllers>`_
 * `Models <#models>`_

------

.. _breaking-changes:
Breaking changes
====

#. response/Train
    * Times of departure and arrival have changed the format to ISO 8601 ('YYYY-MM-DDThh:mm:ss±hh:mm')

#. To unauthorized requests the system used to redirect requests to another url, however now it responds with 403 error with message "Authentication Failed.".

.. _deprecations:
Deprecations
====

request/Person
  * *citizenship* is slightly renamed to *country_of_document* because it is more semantically suitable to RZHD requirements

.. _amends:
Amends
====

.. _controllers:
Controllers
----

FilesController
 * Into *getEticket* has been added a possibility to get file by ticket's ID. New parameter *search_by* helps with it
 * New method *getCancellationForm* has been added to allow users receiving the file

InformationController
 * New method *getRoute*
 * New method *getAvailableMeals*. It allows to fetch list of available meals that can be used for `changeMeal </controllers/TicketsController.rst#changemeal>`_

ReferenceController
 * `documentTypes </controllers/ReferenceController.rst#documenttypes>`_ now has a format's description
 * New methods has been added `additionPlacesRequirements </controllers/ReferenceController.rst#additionplacesrequirements>`_

TicketsController
 * New method `bookPackage </controllers/TicketsController.rst#bookpackage>`_ allows to book few tickets at once.
 * New method `changeMeal </controllers/TicketsController.rst#changemeal>`_ allows to change meal for `Ticket </models/response/Ticket.rst>`_ : meal (if it's provided)

.. _models:
Models
----

request/Selection
 * Few new properties have been added

response/Carriage
 * Availability of few new types of places has been added

response/ServiceClass
 * Information about carriage owner, service tags and few other carriage options have been added

response/Train
 * Information about distance, stations translation, countries of visit and allowed document types have been added

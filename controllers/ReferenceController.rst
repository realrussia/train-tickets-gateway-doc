====
ReferenceController
====

Path:

``/reference/[_methodName_]``

Provides references for all ID returned in system. Some results of this controller can be changed


.. _carriageClasses:
carriageClasses
----
Method: GET

Carriage classes

Example of request:

``/reference/carriageClasses?user=test_user``

Result: `Reference <../models/response/Reference.rst>`_


.. _seatTypes:
seatTypes
----
Method: GET

Seat types

Example of request:

``/reference/seatTypes?user=test_user``

Result: `Reference <../models/response/Reference.rst>`_


.. _documentTypes:
documentTypes
----
Method: GET

Document types of passengers

Example of request:

``/reference/documentTypes?user=test_user``

Result: `Reference <../models/response/Reference.rst>`_


.. _services:
services
----
Method: GET

Services of trains and carriages. In description tag you can see is it service fot trains of for carriages

Example of request:

``/reference/services?user=test_user``

Result: `Reference <../models/response/Reference.rst>`_


.. _deliveries:
deliveries
----
Method: GET

Deliveries used for ordering non electronic tickets

Example of request:

``/reference/deliveries?user=test_user``

Result: `Reference <../models/response/Reference.rst>`_


.. _ticketStatuses:
ticketStatuses
----
Method: GET

Statuses of tickets

Example of request:

``/reference/ticketStatuses?user=test_user``

Result: `Reference <../models/response/Reference.rst>`_


.. _cabinGenderTypes:
cabinGenderTypes
----
Method: GET

Cabin gender type. Used in bookTickets method

Example of request:

``/reference/cabinGenderTypes?user=test_user``

Result: `Reference <../models/response/Reference.rst>`_


.. _registrationTypes:
registrationTypes
----
Method: GET

Registration type

Example of request:

``/reference/registrationTypes?user=test_user``

Result: `Reference <../models/response/Reference.rst>`_


.. _tiers:
tiers
----
Method: GET

Tier of tickets to book. Used in bookTickets method

Example of request:

``/reference/tiers?user=test_user``

Result: `Reference <../models/response/Reference.rst>`_


.. _stations:
stations
----
Method: GET

List of used stations. Description contains country of station in format ISO 3166-1 alpha-2.
NOTE: this list can be different between test server and production

Example of request:

``/reference/stations?user=test_user``

Result: `Reference <../models/response/Reference.rst>`_


.. _tariffs:
tariffs
----
Method: GET

List of used tariffs

Example of request:

``/reference/stations?user=test_user``

Result: `Reference <../models/response/Reference.rst>`_


.. _countries:
countries
----
Method: GET

List of used countries codes. This information should be the same as in format ISO 3166-1 alpha-2.

Example of request:

``/reference/countries?user=test_user``

Result: `Reference <../models/response/Reference.rst>`_


.. _additionalPlacesRequirements:
additionalPlacesRequirements
----
Method: GET

Additional places requirements. Used in bookTickets method.
If value of description == 1 then this options is allowed for third class only

Example of request:

``/reference/additionalPlacesRequirements?user=test_user``

Result: `Reference <../models/response/Reference.rst>`_


====
TicketsController
====

Path:

``/tickets/[_methodName_]``

Provides methods for booking, confirming, declining, cancelling and editing tickets, as well as changing the registration type.


.. _bookTickets:
bookTickets
----
Method: POST

Use this method to start the booking operation. If successful, a temporary order will be created and selected places will be reserved.

Parameters:

* params - Contain XML with tickets details. See `Model <../models/request/BookTickets.rst>`_ specification and `example <../examples/bookTickets.xml>`_ in XML-format

Example of request:

``/tickets/bookTicket``

Result: `Train <../models/response/Train.rst>`_


.. _confirm:
confirm
----
Method: GET

Use this method to confirm an incomplete booking (bookTickets_). After confirmation, a permanent order will be created and money will be taken from your account.

Parameters:

* sid - ID of temporary order

Example of request:

``/tickets/confirm?user=acp_test&sid=92``

Result: `CancellationResult <../models/response/CancellationResult.rst>`_


.. _decline:
decline
----
Method: GET

Use this method to decline an incomplete booking (bookTickets_). After confirmation the permanent order will be removed. Orders which are not confirmed will be automatically declined after 15 minutes.

Parameters:

* sid - ID of temporary order

Example of request:

``/tickets/decline?user=acp_test&sid=92``

Result: `SimpleOperationResult <../models/response/SimpleOperationResult.rst>`_


.. _cancel:
cancel
----
Method: GET

Use this method to cancel tickets from a permanent order.

Parameters:

* tickets - IDs of tickets divided by ","

Example of request:

``/tickets/cancel?user=acp_test&tickets=279,280``

Result: `SimpleOperationResult <../models/response/SimpleOperationResult.rst>`_


.. _changeRegistrationType:
changeRegistrationType
----
Method: GET

Use this method to change the registration type of passed tickets.

Parameters:

* tickets - IDs of tickets divided by ","
* registrationType - registration type ID

Example of request:

``/tickets/changeRegistrationType?user=acp_test&tickets=280,281&registrationType=2``

Result: `SimpleOperationResult <../models/response/SimpleOperationResult.rst>`_


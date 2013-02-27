====
TicketsController
====

Path:

``/tickets/[_methodName_]``

Provide methods for booking, cancellation, editing tickets etc.

.. _bookTickets:
bookTickets
----
Method: POST

Using this method you start thr booking operation. To finish it you should use confirm_ or decline_. After successful booking will be created temporary order and selected places will be reserved. Use his ID to cancel or decline it.

Parameters:

* params - Contain XML with tickets details. `Model <../models/request/BookTickets.rst>`_. `Example <examples/bookTickets.xml>`_;

Example of request:

``/tickets/bookTicket``

Result: `Train <../models/response/Train.rst>`_

.. _confirm:
confirm
----
Method: GET

Use this method to confirm incomplete booking operation (bookTickets_). After confirmation will be created permanent order and money will be taken from your deposit.

Parameters:

* sid - ID of temporary order;

Example of request:

``/tickets/confirm?user=acp_test&sid=92``

Result: `CancellationResult <../models/response/CancellationResult.rst>`_

.. _decline:
decline
----
Method: GET

Use this method to decline incomplete booking operation (bookTickets_). After confirmation will be removed permanent order. Order will be automatically declined after 15 minutes.

Parameters:

* sid - ID of temporary order;

Example of request:

``/tickets/decline?user=acp_test&sid=92``

Result: `SimpleOperationResult <../models/response/SimpleOperationResult.rst>`_

.. _cancel:
cancel
----
Method: GET

Cancellation tickets of permanent order.

Parameters:

* tickets - IDs of tickets divided by ",";

Example of request:

``/tickets/cancel?user=acp_test&tickets=279,280``

Result: `SimpleOperationResult <../models/response/SimpleOperationResult.rst>`_

.. _changeRegistrationType:
changeRegistrationType
----
Method: GET

Changing of registration type of passed tickets.

Parameters:

* tickets - IDs of tickets divided by ",";
* registrationType - registration type ID;

Example of request:

``/tickets/changeRegistrationType?user=acp_test&tickets=280,281&registrationType=2``

Result: `SimpleOperationResult <../models/response/SimpleOperationResult.rst>`_

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
    See `additional notes </articles/bookTicketsNotes.rst>`_ for this method.
    The permanent order is also created at this stage with partial data about the booking.

Parameters:

* params - Contain XML with tickets details. See `Model <../models/request/BookTickets.rst>`_ specification and `example <../examples/bookTickets.xml>`_ in XML-format

Example of request:

``/tickets/bookTickets``

Result: `BookTicketsResult <../models/response/BookTicketsResult.rst>`_


.. _confirm:
confirm
----
Method: GET

Use this method to confirm an incomplete booking (bookTickets_). After confirmation, a permanent order will receive all necessary and money will be taken from your account.
    If some problems with confirmation occur the permanent order will be marked as successful and money will be taken from your account.
    To update the incorrect confirmed order it needs to resend the confirmation request. Or contact out support
    See `problems on confirmation </articles/problemsOnConfirmation.rst>`_ for more details

Parameters:

* sid - ID of temporary order

Example of request:

``/tickets/confirm?user=test_user&sid=92``

Result: `ConfirmationResult <../models/response/ConfirmationResult.rst>`_


.. _decline:
decline
----
Method: GET

Use this method to decline an incomplete booking (bookTickets_). After confirmation the permanent order will be removed. Orders which are not confirmed will be automatically declined after 15 minutes.

Parameters:

* sid - ID of temporary order

Example of request:

``/tickets/decline?user=test_user&sid=92``

Result: `SimpleOperationResult <../models/response/SimpleOperationResult.rst>`_


.. _cancel:
cancel
----
Method: GET

Use this method to cancel tickets from a permanent order.

Parameters:

* tickets - IDs of tickets divided by ","

Example of request:

``/tickets/cancel?user=test_user&tickets=279,280``

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

``/tickets/changeRegistrationType?user=test_user&tickets=280,281&registrationType=2``

Result: `SimpleOperationResult <../models/response/SimpleOperationResult.rst>`_


.. _orderTickets:
orderTickets
----
Method: POST

This method used for creation of manually processed orders.

Parameters:

* params - Contain XML with tickets details. See `Model <../models/request/OrderTickets.rst>`_ specification and `example <../examples/orderTickets.xml>`_ in XML-format

Example of request:

``/tickets/orderTickets``

Result: `OrderTicketsResult <../models/response/OrderTicketsResult.rst>`_


.. _bookPackage:
bookPackage
----
Method: POST

The method for booking of several request in one time

Parameters:

* params - Contain XML with tickets details. See `Model <../models/request/BookPackage.rst>`_ specification

Example of request:

``/tickets/bookPackage``

Result: `BookPackageResult <../models/response/BookPackageResult.rst>`_


.. _changeMeal:
changeMeal
----
Method: GET

Use this method to change the meal of passed ticket.

Parameters:

* ticket - ID of ticket
* mealCode - code of meal received from `AvailableMeals <../models/response/AvailableMeals.rst>`_

Example of request:

``/tickets/changeMeal?user=test_user&id=280&mealCode=В``

Result: `SimpleOperationResult <../models/response/SimpleOperationResult.rst>`_


.. _checkTransactionStatus:
checkTransactionStatus
----
Method: GET

Use this method to check status of your transaction by id of temporary order.

Parameters:

* sid - ID of temporary order

Example of request:

``/tickets/checkTransactionStatus?user=test_user&sid=92``

Result: Return 0 if transaction is successful, 1 if transaction is in progress, 2 if there is an error transaction


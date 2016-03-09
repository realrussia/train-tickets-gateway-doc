====
InformationController
====

Path:

``/information/[_methodName_]``

Provides information such as schedules, trains, orders, availability and reports.


.. _getSchedule:
getSchedule
----
Method: GET

Provides information about the available trains for a selected route and date.

Parameters:

* st1 - Id of station of departure
* st2 - Id of station of arrival
* dt - date in format `dd.mm.YYYY`

Example of request:

``/information/getSchedule?&user=username&dt=28.03.2013&st1=8631&st2=11783``

Result: `Schedule <../models/response/Schedule.rst>`_


.. _getTrain:
getTrain
----
Method: GET

Provides information about the available places on a requested train.

Parameters:

* st1 - Id of station of departure
* st2 - Id of station of arrival
* dt - date in format `dd.mm.YYYY`
* train - train number. Train number has to be `transliterated </articles/trainNumbers.rst>`_

Example of request:

``/information/getTrain?&user=username&dt=28.03.2013&st1=8631&st2=11783&train=020U``

Result: `Train <../models/response/Train.rst>`_


.. _getOrder:
getOrder
----
Method: GET

Provides information about the tickets and statuses of a permanent order.
**Note**: this method used for orders created via `TicketsController::BookTickets <TicketsController.rst#booktickets>`_

Parameters:

* id - Reference number of order

Example of request:

``/information/getOrder?user=username&id=10174``

Result: `Order <../models/response/Order.rst>`_


.. _getOrderRequested:
getOrderRequested
----
Method: GET

Provides information about the tickets and statuses of a permanent order.
**Note**: this method used for orders created via `TicketsController::OrderTickets <TicketsController.rst#ordertickets>`_

Parameters:

* id - Reference number of order

Example of request:

``/information/getOrderRequested?user=username&id=10174``

Result: `OrderRequested <../models/response/OrderRequested.rst>`_


.. _getReport:
getReport
----
Method: GET

Provides a report on operations during a selected period; which includes:

* Ticket booking;
* Ticket cancellation;
* Funds which have been deposited

Parameters:

* dt1 - First time bound
* dt2 - Second time bound

Parameters should be in format `dd.mm.YYYY`

Dates interprets as GMT+0

Time of first bound = 00:00, and the second = 23:59


Example of request:

``/information/getReport?user=username&dt1=01.01.2013&dt2=01.03.2013``

Result: `Report <../models/reports/tickets/Report.rst>`_


.. _getRoute:
getRoute
----
Method: GET

Provides information about stations the train goes through

Parameters:

* st1 - Id of station of departure
* st2 - Id of station of arrival
* dt - date in format `dd.mm.YYYY`
* train - train number. Train number has to be `transliterated </articles/trainNumbers.rst>`_


Example of request:

``/information/getRoute?&user=username&dt=28.03.2013&st1=8631&st2=11783&train=020U``

Result: `Route <../models/response/Route.rst>`_


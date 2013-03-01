====
InformationController
====

Path:

``/information/[_methodName_]``

Provide different information.

.. _getSchedule:
getSchedule
----
Method: GET

Information about available trains for passed route and date

Parameters:

* st1 - Id of station of departure;
* st2 - Id of station of arrival;
* dt - date in format `dd.mm.YYYY`

Example of request:

``/information/getSchedule?&user=username&dt=28032013&st1=8631&st2=11783``

Result: `Schedule <../models/response/Schedule.rst>`_

.. _getTrain:
getTrain
----
Method: GET

Information about available places on requested train

Parameters:

* st1 - Id of station of departure;
* st2 - Id of station of arrival;
* dt - date in format `dd.mm.YYYY`
* train - train number. At the moment with cyrillic litter in the end.

Example of request:

``/information/getTrain?&user=username&dt=28032013&st1=8631&st2=11783&train=020%D0%A3``

Result: `Train <../models/response/Train.rst>`_

.. _getOrder:
getOrder
----
Method: GET

Information about permanent order. Here you can find information about tickets ant their statuses.

Parameters:

* id - Reference number of order.

Example of request:

``/information/getOrder?user=username&id=10174``

Result: [Order](../models/response/Order.rst)

.. _getReport:
getReport
----
Method: GET

Report for operation during selected period. It include:

* tickets booking;
* tickets cancellation;
* money operations (funds to you deposit).

Parameters:

* dt1 - First time bound
* dt2 - Second time bound

Parameters should be in format `dd.mm.YYYY`. Dates interprets as GMT+0. Time of first bound = 00:00, and the second = 23:59

Example of request:

``/information/getReport?user=username&dt1=01.01.2013&dt2=01.03.2013``

Result: [Order](../models/reports/tickets/Report.rst)

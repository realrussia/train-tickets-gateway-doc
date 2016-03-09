====
FilesController
====

Path:

``/files/[_methodName_]``

Provides files for downloading


.. _getEticket:
getEticket
----
Method: GET

Provides PDF file of eticket. NOTE: in case of error method will return `Error <../models/response/Error.rst>`_

Parameters:

* id - Reference number of order
* search_by - Not required. Enum of ['order', 'ticket']. Set the entity that will be used for E-Ticket search

Example of request:

``/files/getEticket?user=username&id=10174``

Result: PDF-file


.. _refreshFiles:
refreshFiles
----
Method: GET

Files are cached on our server. Sometimes files become outdated. This method renews files.

Parameters:

* id - Reference number of order

Example of request:

``/files/refreshFiles?user=test_user&id=10174``

Result: `SimpleOperationResult <../models/response/SimpleOperationResult.rst>`_


# Tickets controller

Path:

```
/tickets/[_methodName_]
```

Provide methods for booking, cancellation, editing tickets etc.

Available methods:

 * [bookTickets][]
 * [confirm][]
 * [decline][]
 * [cancel][]
 * [changeRegistrationType][]

[bookTickets]: #bookTickets ""
[confirm]: #confirm ""
[decline]: #decline ""
[cancel]: #cancel  ""
[changeRegistrationType]: #changeRegistrationType ""

## <a id="bookTickets">bookTickets</a>

Using this method you start thr booking operation. To finish it you should use [confirm][] or [decline][]. After successful booking will be created temporaty order and selected places will be reserved. Use his ID to cancel or decline it.

Method: POST

Parameters:

 * params - Contain XML with tickets details [Model](models/request/BookTickets.rst) [Example](examples/bookTickets.xml);

Example of request:

```
/tickets/bookTicket
```

Result: [Train](models/response/Train.rst)

## <a id="confirm">confirm</a>

Use this method to confirm incomplete booking operation ([bookTickets][]). After confirmation will be created permanent order and money will be takken from your deposit.

Method: GET

Parameters:

 * sid - ID of temporary order;

Example of request:

```
/tickets/confirm?user=acp_test&sid=92
```

Result: [CancellationResult](models/response/CancellationResult.rst)

## <a id="decline">decline</a>

Use this method to decline incomplete booking operation ([bookTickets][]). After confirmation will be removed permanent order. Order will be automaticaly declined after 15 minutes.

Method: GET

Parameters:

 * sid - ID of temporary order;

Example of request:

```
/tickets/decline?user=acp_test&sid=92
```

Result: [SimpleOperationResult](models/response/SimpleOperationResult.rst)

## <a id="cancel">cancel</a>

Cancellation tickets of permanent order.

Method: GET

Parameters:

 * tickets - IDs of tickets divided by ",";

Example of request:

```
/tickets/cancel?user=acp_test&tickets=279,280
```

## <a id="changeRegistrationType">changeRegistrationType</a>

Changing of registration type of passed tickets.

Method: GET

Parameters:

 * tickets - IDs of tickets divided by ",";
 * registrationType - registration type ID;

Example of request:

```
/tickets/changeRegistrationType?user=acp_test&tickets=280,281&registrationType=2
```
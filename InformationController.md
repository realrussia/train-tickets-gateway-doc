# Information controller

Path:

```
/information/[_methodName_]
```

Provide different information.

Available methods:

 * [getTrain][]
 * [getOrder][]
 * [getReport][]

[getTrain]: #getTrain ""
[getOrder]: #getOrder ""
[getReport]: #getReport ""


## <a id="getTrain">getTrain</a>

Information about available places on requested train

Method: GET

Parameters:

 * st1 - Id of station of departure;
 * st2 - Id of station of arrival;
 * dt - date in format `dd.mm.YYYY`
 * train - train number. At the moment with cyrillic litter in the end.

Example of request:

```
 /information/getTrain?&user=username&dt=28032013&st1=8631&st2=11783&train=020%D0%A3
```

Result: [Train](models/response/Train.rst)

## <a id="getOrder">getOrder</a>

Information about permanent order. Here you can find information about tickets ant their statuses.

Method: GET

Paramenters:

 * id - Reference number of order.

Example of requst:

```
/information/getOrder?user=username&id=10174
```

Result: [Order](models/response/Order.rst)

## <a id="getReport">getReport</a>

Report for operation during selected period. It include:

 * tickets booking;
 * tickets cancellation;
 * money operations (funds to you deposit).

Method: GET

Parameters:

 * dt1 - First time bound
 * dt2 - Second time bound

Parameters should be in format `dd.mm.YYYY`. Dates interpretes as GMT+0. Time of first bound = 00:00, and the second = 23:59

Example of requst:

```
/information/getReport?user=username&dt1=01.01.2013&dt2=01.03.2013
```

Result: [Order](models/reports/tickets/Report.rst)
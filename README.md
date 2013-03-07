
#This is the documentation for TrainsTicketsGateway

To use this gateway you need to [contact us](manager) and get _username_.

Gateway has 2 controllers:

 * [Information][]
 * [Tickets][]

[Information]: controllers/InformationController.rst "Specification of Information controller"
[Tickets]: controllers/TicketsController.rst "Specification of Tickets controller"

For any technical queries please contact [developer's email](developer)

For all other queries please contact [manager's email](manager)

[developer]: victor@realrussia.co.uk "Developer's email"
[manager]: info@realrussia.co.uk "Manager's email"

##Notes

Result of all methods of controllers is **xml**.

Each request (GET and POST) must be accompanied with your _username_ which we have provided you with. Examples are present in specifications of each method.

If error has occurred during process of request then method should return an [Error](/models/response/Error.rst).

Some tickets can be cancelled by clients themselves. To take information about cancelled tickets use [getReport](/controllers/InformationController.rst#getReport)

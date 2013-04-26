#This is the documentation for the TrainsTicketsGateway

Before using this gateway you need to contact us (<info@realrussia.co.uk>) and get your _username_.

This Gateway has 3 controllers:

 * [Information][]
 * [Tickets][]
 * [Reference][]

[Information]: controllers/InformationController.rst "Specification of Information controller"
[Tickets]: controllers/TicketsController.rst "Specification of Tickets controller"
[Reference]: controllers/ReferenceController.rst "Reference book for all IDs used in system"

For any technical queries please contact <victor@realrussia.co.uk>

For all other queries please contact <info@realrussia.co.uk>

##Notes

Result of all methods of controllers is in **xml** format.

Each request (GET and POST) must be accompanied with your _username_ which has been provided. 

Examples are present within the specifications of each method.

If an error has occurred during the request process, this should return an [Error](/models/response/Error.rst). [List of possible errors](errors.rst).

Certain tickets can be cancelled by clients themselves, for information about cancelled tickets use [getReport](/controllers/InformationController.rst#getreport)

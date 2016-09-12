#This is the documentation for the TrainsTicketsGateway

Before using this gateway you need to contact us (<support@realrussia.co.uk>) and get your _username_.

This Gateway has 4 controllers:

 * [Information][]
 * [Tickets][]
 * [Reference][]
 * [Files][]

[Information]: ./controllers/InformationController.rst "Specification of Information controller"
[Tickets]: ./controllers/TicketsController.rst "Specification of Tickets controller"
[Reference]: ./controllers/ReferenceController.rst "Reference book for all IDs used in system"
[Files]: ./controllers/FilesController.rst "Files for downloading"

For all queries please contact <support@realrussia.co.uk>

##Notes

Result of all methods of controllers is in **xml** format, excluding FilesController.

Each request (GET and POST) must be accompanied with your _username_ which has been provided. 

Examples are present within the specifications of each method.

If an error has occurred during the request process, this should return an [Error](./models/response/Error.rst). [List of possible errors](./articles/errors.rst).

Certain tickets can be cancelled by clients themselves, for information about cancelled tickets use [getReport](./controllers/InformationController.rst#getreport)

## Release notes

###09.09.2016

 * An adding of [migration notes for v2](./articles/v2-migration-notes.rst)
 * New property [Ticket](./models/response/Ticket.rst):meal added. Also a [method of changing](./controllers/TicketsController.rst#changemeal) added
 * Booking of the whole coupe. [Selection](./models/request/Selection.rst):book_the_whole_coupe
 * [Person](./models/request/Person.rst):country_of_document
 * [documentTypes](./controllers/ReferenceController.rst#documenttypes) a format's description added
 * [getCancellationBlank](./controllers/FilesController.rst#getcancellationblank). New method added 
 * Update of [errors list](./articles/errors.rst)

###15.03.2016 - v2

 * Update of protocol to v2
 * To unauthorized requests system used to redirect to another url, but now it responds with 403 error with message "Authentication Failed.".   

###29.09.2015

 * Under new requirements from RZHD a format of passengers data had changed. For [Person](./models/request/Person.rst) field place_of_birth is removed.
 
###26.05.2015

 * For "Seat only" carriage class the option [Selection](./models/request/Selection.rst):in_one_kupe forced to 0.

###09.12.2013

 * Under new requirements from RZHD a format of passengers data had changed. For [Person](./models/request/Person.rst) field country_of_birth is changed to place_of_birth.

###06.12.2013

 * RZHD had changed format of hierarchy between passengers and tickets in request for Grand carriages. [Example of request](/examples/bookTicketsGrand.xml)
 * For [request](./models/request/BookTickets.rst) in [bookTickets](./controllers/TicketsController.rst#booktickets) need to specify train number that returned by [getTrain](./controllers/InformationController.rst#gettrain) in [Train.ServiceClass.trainThreadNumber](./models/response/ServiceClass.rst)

-------------------------------
Art\\Models\\XmlGateway\\Ticket
-------------------------------

.. php:namespace: Art\\Models\\XmlGateway

.. php:class:: Ticket

    My short description

    Full description here

    .. php:attr:: publicProperty

        string

    .. php:attr:: ticketId

        int

    .. php:attr:: registrationType

    .. php:attr:: status

    .. php:attr:: placeNumber

    .. php:attr:: price

        Price

    .. php:attr:: bookingDate

    .. php:attr:: cancellationDate

    .. php:attr:: passengers

        Person[]

    .. php:method:: __construct($ticketId, $registrationType, $status, $placeNumber, $bookingDate, $cancellationDate, $price, $passengers)

        My constructor

        :type $ticketId: int
        :param $ticketId: the ID
        :param $registrationType:
        :param $status:
        :param $placeNumber:
        :param $bookingDate:
        :param $cancellationDate:
        :param $price:
        :param $passengers:

#BookTicketsResult

 Temporary booking order. It will be removed after confirmation or declination

 1.  int **preOrderId** Id of temporary booking order;

 1.  [Train](Train.rst) **train**;

 1.  string **buyingTime** Time of request;

 1.  string **carriageNumber**;

 1.  int **carriageClassId**;

 1.  int **cabinGenderType**;

 1.  int **placesCount**;

 1.  float **price**;

 1.  [BookingCacheTicket](BookingCacheTicket.rst)[] **tickets**;

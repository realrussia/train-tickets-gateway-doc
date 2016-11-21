====
BookingCacheTicket
====

    Temporary booking ticket

#.  string **place_number** Can be empty for child without places;

#.  int **places_count**;

#.  `Person <Person.rst>`_\[] **passengers**;

#.  float **price**;

#.  float **cost**;

#.  float **nds**;

#.  string **tariff** Tariff code. We avoid to use an identifier here because RZHD often adds new tariffs unexpectedly.
It leads the differences between our reference books.
Without hard link of tariffs in `Tariffs <../../controllers/ReferenceController.rst#tariffs>`_ with your database
we are able to add new tariffs on the fly and just throw you a code.;

#.  int **tier**;


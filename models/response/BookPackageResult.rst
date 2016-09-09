====
BookPackageResult
====

    Temporary booking order. It will be removed after confirmation or declination

#.  string **order_id** Id (reference number) of permanent order;

#.  `\Art\Classes\ValuesCollection <\Art\Classes\ValuesCollection.rst>`_ **price_collection**;

#.  `\Art\Classes\ValuesCollection <\Art\Classes\ValuesCollection.rst>`_ **cost_collection**;

#.  `BookTicketsResult <BookTicketsResult.rst>`_\[] **results** Collection of results;


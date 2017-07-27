====
Problems on confirmation
====

The booking process consists of two parts:

 * booking request
 * confirmation

If there are some problems on the confirmation stage after the order is confirmed on the RZHD's side, but not on the partner's side.
For partners, it looks like he can stop the process without any payment, but for us the order already costs.

To avoid the situation we create the permanent order together with the temporary booking order.
If the confirmation is successful we just update it with booking data.
If the temporary order is refused then we mark the permanent order as canceled.
And if confirmation was finished with undefined result or network error, then the permanent order will be marked as
booked and money will be taken from the partner's account until the successful confirmation attempt or manual solving of the situation by the support


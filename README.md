# Payment Gateway

#### # No Cash Payment Method. Use the Paid Button to toggle dues to paid.
#### # No Customer's Payment Submit for operator.
#### # Gateway is enabled globally.
#### # Super Admin, Group Admin and Operator can have Payment Gateway.
#### # Group Admin or Operator will inherit payment gateways if they have no payment gateway.
#### # Each Product(Internet Package, Software, SMS) will have payment controller and responsible for call payment gateway controller.
#### # Payment Create Route for each product will receive instance of payment gateway and instance of invoice.

### # There are two types of payment gateway.
* Online
* Recharge Card

### # Important method of payment gateway.

* getInternetPaymentGws(operator $operator){}
  * If operator has many payment gateways return the payment gateways.
  * If group admin of the operator has many payment gateways return the payment gateways.
  * If Super Admin of the operator has many payment gateways return the payment gateways.
  * Return must be instance of payment gateway if has payment gateways.
  

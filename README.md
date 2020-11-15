# Payment Gateway

#### # No Cash Payment Method. Use the Paid Button to toggle dues to paid.
#### # No Customer's Payment Submit for operator.
#### # Gateway is enabled globally.
#### # Super Admin, Group Admin and Operator can have Payment Gateway.
#### # Group Admin or Operator will inherit payment gateways if they have no payment gateway.
#### # Payment Create Route for each product will receive instance of payment gateway and instance of invoice.
#### # Each Product(Internet Package, Software, SMS) will have payment controller and responsible for call payment gateway controller.

### # There are two types of payment gateway.
* Online
* Recharge Card

### # Three important methods of payment gateway.
* isMerchant(operator $operator) {}
  * Is the operator has many payment gateways.
  * Return is boolean
  
* getMerchant(payment_gateway $payment_gateway){}
  * Return operator instance of the payment gateway

* getPaymentGws(operator $operator, string $pay_for){}
  * If operator has many payment gateways return the payment gateways.
  * If group admin of the operator has many payment gateways return the payment gateways.
  * If Super Admin of the operator has many payment gateways return the payment gateways.
  * Return must be instance of payment gateway if has payment gateways.
  

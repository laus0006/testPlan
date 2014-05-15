This is a test plan for a supermarket self-service checkout system. This system is responsible, through interactions with the customer, for scanning in items and displaying an accurate total cost, then accepting payment from the customer.

There are several components to the system: 

	Display - A touchscreen input/output device for interacting with the user. Includes the user interface.
	Speaker - Auditory input/output, including alarm.
	Barcode Scanner - Reads the barcode label on the product into a computer readable code.
	Product Scale - For products priced by weight, measures the total weight of the item.
	Baggage Area - Holds the bag, and checks that items have been inserted into the bag.
	Payment Interface - Displays total payment required, and enables several forms of payment, including credit card and cash.
	Control System - The software inside of the checkout system that manages all other components. 
	
The Payment Interface is a complicated piece of the product. It has both input and output components, including:
Input - cash note input, cash coin input, credit card reader with buttons,
Output - receipt printer, cash note output, cash coin output.

Additionally, the system is connected to an external database that holds pricing information for the products, and to a payment system for electronic payments.

The primary risk for the system is that customers are either overcharged or undercharged. An overcharge may result in a few lawsuits, and an undercharge would cost the client a significant amount of money over time. A secondary risk is that the system is perceived as too much effort to use, and customers will not use the self-service checkout.

The components are ordered by potential for risk, highest first

	Control System - If the components of the system don't integrate properly, there will be massive problems.
	Payment Interface - The whole point of the device is to receive money. This must register payments properly.
	Display - The user interface must be simple to use and understand.
	Speaker - If the customer leaves without paying, an alarm must sound, to reduce monetary losses.
	Baggage Area - It is only necessary to know if an unexpected weight is in the bag.
	Product Scale - A small minority of products must be weighed.
	Barcode Scanner - The product must be correctly found in the database. An inaccurate barcode scanner would match wrong products.

Many of the components in the self-service checkout system are already in use in other applications. Manual checkouts already use barcode scanners, scales, and credit card scanners in an automatic way, indicating that these are lower risk areas. 

Most important tests:

	Unit Testing:
	While the simple components would not be complicated to design, it is important to verify they function properly individually before integrating them together. An emphasis on testing the components of the payment system is necessary, because of the money aspect.

	Integration Testing:
	The payment interface and the control system depend on the integration of many components. These components themselves are quite simple, however, integration testing is extremely important so that, for example, the dollar value of an item doesn't lose an order of magnitude while it is being processed. 

	User acceptance testing:
	The client wants it's customers to use the self-service checkouts, to save money. If these customers don't find the system acceptable, the entire project has been an exercise in futility, and a waste of money. 

Less important tests (Though they all have their own benefits):

	Fuzz testing:
	The users of the system do not have access to a command console, or direct control over the system, limiting the range of input that is possible. 

	Compatibility testing:
	Given the specialist build of the self-service system, it is unlikely that it would need to be compatible with any older systems.

	Load testing:
	There is a limit of one customer at a time on the system, and each customer, is likely to have less than 50 items, indicating that load will not be a problem when the system is in the field.
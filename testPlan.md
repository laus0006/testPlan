This is a test plan for a supermarket self-service checkout system. This system is responsible, through interactions with the customer, for scanning in items and displaying an accurate total cost, then accepting payment from the customer.

There are several components to the system: 

	Display - A touchscreen input/output device for interacting with the user. Includes the user interface.
	Speaker - Auditory input/output, including alarm.
	Barcode Scanner - Reads the barcode label on the product into a computer readable code.
	Product weigher - For products priced by weight, measures the total weight of the item.
	Baggage area - Holds the bag, and checks that items have been inserted into the bag.
	Payment interface - Displays total payment required, and enables several forms of payment, including credit card and cash.

Additionally, the system is connected to an external database that holds pricing information for the products, and to a payment system for electronic payments.

The primary risk for the system is that customers are either overcharged or undercharged. An overcharge may result in a few lawsuits, and an undercharge would cost the client a significant amount of money over time.

The components are ordered by potential for risk, highest first

	Payment Interface - The whole point of the device is to receive money. This must register payments properly.
	Barcode Scanner - The product must be correctly found in the database. An inaccurate barcode scanner would match wrong products.
	Display - The user interface must be simple to use and understand.
	Product Weighter - A small minority of products must be weighed.
	Baggage Area - It is only necessary to know if an unexpected weight is in the bag.
	
Given that these components are fairly simple by themselves, it would be appropriate to test and develop each component individually first, and integrate at a later stage. 
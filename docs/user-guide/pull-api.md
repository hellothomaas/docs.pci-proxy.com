### General understanding
The pull operation is to fetch new bookings from Sales Channels. You make a HTTPS request to Datatrans'
PCI Proxy, the PCI Proxy will forward the request to the Sales Channel and return
the response to you. Before returning the response to your application, the PCI Proxy will parse and
clean it by locating the card numbers, using the specified expressions, and
replace them with corresponding aliases. 

### Supported HTTP methods
* GET
* POST
* PUT
* PATCH
* HEAD
* DELETE
### General understanding
The push operation is to receive HTTPS requests from a Channel Partner.
Datatrans sets up a specific PUSH URL for you. The Channel Partner sends (pushes) the
request to that PUSH URL. Before forwarding the request to your application, the PCI Proxy will parse and
clean it by locating the card numbers, using the specified expressions, and replace them with corresponding aliases.

### Setup information
In order to setup and configure the PUSH URL, we need the following information:

| Data                | Description                                                                                | 
| ------------------- | ------------------------------------------------------------------------------------------ | 
| **Target URL**      | Where should the parsed information to be forwarded to (your application)?                 | 
| **Example Request** | In order to be able to use XPath to detect credit cards and parse it correspondingly       | 
| **IP Address**      | Which IP will send us the push messages? (Whitelist to prevent others to send us requests) |
 
 An example request could look like:
 
     <?xml version="1.0" encoding="UTF-8"?>
     <Reservation>
       ...
       <Payment>
         <CardNumber>4242 4242 4242 4242</CardNumber>
         ...
       </Payment>
       ...
     </Reservation>

### Getting started
Once your PUSH URL has been set up by Datatrans, your Channel Partner has to send the requests to
the predefined PUSH URL for PCI Proxy Push operation instead of directly to you.
**Hence, channel is PCI compliant.**

#### PUSH URL for PCI Proxy Push Operation
| Environment | URL           | 
| ----------- | ------------- | 
| TEST        | https://**pilot**.datatrans.biz/upp/proxy/push/`{YOUR-SPECIFIC-KEY}` | 
| PROD        | https://**payment**.datatrans.biz/upp/proxy/push/`{YOUR-SPECIFIC-KEY}`      |

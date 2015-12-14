### General Understanding
Our Payment Pages are different web interfaces (APIs) that can be used to tokenize
credit card numbers. For instance, it can be used in the reservation process to guarantee a booking.  

Through our APIs, the guest’s computer communicates directly with our servers to exchange
its credit card number for a credit card token and forwards only the token to your servers.
**Hence, channel is PCI compliant**.

### Responsive Payment Page & Inline Mode
Redirect Mode| Lightbox Mode        | Inline Mode 
:------------:|:--------------------:|:-----------:
<img src="../../img/redirect.png" width="150"> | <img src="../../img/lightbox.png" width="150"> | <img src="../../img/inline.png" width="150">      
Redirect of consumer to payment page managed by Datatrans. | Payment pages are placed on shop as overlay (iFrame). | Payment page managed by Datatrans is incorporated with iFrame.    
[Demo + Code Sample](https://www.datatrans.ch/showcase/authorisation/redirect-mode) | [Demo + Code Sample](https://www.datatrans.ch/showcase/authorisation/lightbox-mode) | [Demo + Code Sample](https://www.datatrans.ch/showcase/authorisation/inline-mode)

A comprehensive documentation of our Payment pages can be found on our [Showcase](https://datatrans.ch/showcase/authorisation/redirect-mode)

### Getting started
In order to generate an alias with one of the 3 integration variants, please include the following parameter:

| Parameter      | Description                                                        | Example value
| -------------- | -------------------------------------------------------------------| ---
| `uppAliasOnly` | Credit card data is tokenized without authorization and settlement | yes

For example for the redirect mode:

    https://pilot.datatrans.biz/upp/jsp/upStart.jsp
      ?merchantId=1000011011
      &currency=CHF
      &refno=809363
      &paymentmethod=VIS
      &uppAliasOnly=yes

Once the consumer submits the payment form, the response to the SUCCESS/POST URL
contains the `aliasCC` parameter. Save this token within your database.


---


<!--

# Inbound: Push Operation (XML/SOAP API)

# Inbound: Pull Operation (XML/SOAP API)

# Outbound: Web Interface (NoShow)

-->
# Braintree-nonce-JSCode
braintree payments to create nonce from client id :: Testing purpose browser java script code.

### Braintree architecture
Braintree typical architecture says payment from mobile phones we have to follow this step:

Required
- Server (Ruby/php/node/.net/java etc) has credentials of braintree merchant (Sandbox[testing] and live).

- Client (mobile phones : iOS/Android or web : Javascript) has braintree SDK.

FLOW
1. Client first hit a server api for clientToken; server creates that client token on the credentials stored in server(sandbox and live)

1. Client uses that client token to tokenize credit card of USER(customer) using braintree SDK. [That token always changes for same credit card.]

1. Now that token (usually says `payment_method_nonce`) to server using API.

1. Now server uses this token to validate and create payment in braintree server.


### Inside
- For the Flow 2nd step testing use `BraintreeDemoJS.html`
- For the Flow 1st step preparing the demo page. But for now `BraintreeDemoJS.html` uses dummy clientToken.

### Dummy Data

- Any Future date for expiry date
- Any CVV Number
- Credit card

| Test Value | Card Type |
|:--------------------:|:--------------------:|
| 4111 1111 1111 1111 |	Visa |
| 4005519200000004 | Visa |
| 4009348888881881 | Visa |
| 4012000033330026 | Visa |
| 4012000077777777 | Visa |
| 4012888888881881 | Visa |
| 4217651111111119 | Visa |
| 4500600000000061 | Visa |
| 378282246310005	| American Express |
| 371449635398431	| American Express |
| 6011111111111117 | Discover |
| 3530111333300000 |	JCB |
| 6304000000000000 |	Maestro |
| 5555555555554444 |	Mastercard |

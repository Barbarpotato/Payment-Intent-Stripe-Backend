# Payment-Intent-Stripe-Backend
Learn How to make server-side code checkout form to complete various payments


## Set up the server
Install the Stripe Node library:
```js
npm install --save stripe
```

## Create a PaymentIntent
Add an endpoint on your server that creates a PaymentIntent. A PaymentIntent tracks the customer’s payment lifecycle, keeping track of any failed payment attempts and ensuring the customer is only charged once. Return the PaymentIntent’s client secret in the response to finish the payment on the client.

## Configure payment methods
With automatic_payment_methods enabled, we enable cards and other common payment methods for you by default, and you can enable or disable payment methods directly in the Stripe Dashboard. Before displaying the payment form, Stripe evaluates the currency, payment method restrictions, and other parameters to determine the list of supported payment methods. We prioritize payment methods that help increase conversion and are most relevant to the currency and the customer’s location.
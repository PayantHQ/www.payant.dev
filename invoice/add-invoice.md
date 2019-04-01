# Add Invoice

{% api-method method="post" host="" path="https://api.payant.ng/invoices" %}
{% api-method-summary %}
Add Invoice
{% endapi-method-summary %}

{% api-method-description %}
Add Invoices
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="client" type="array" required=true %}
Client Data
{% endapi-method-parameter %}

{% api-method-parameter name="company\_name" type="string" required=true %}
Client's company name
{% endapi-method-parameter %}

{% api-method-parameter name="first\_name" type="string" required=true %}
Client's first name
{% endapi-method-parameter %}

{% api-method-parameter name="last\_name" type="string" required=true %}
Client's last name
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=true %}
Client's email
{% endapi-method-parameter %}

{% api-method-parameter name="phone" type="string" required=true %}
Client's phone number
{% endapi-method-parameter %}

{% api-method-parameter name="address" type="string" required=false %}
Client's address
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=false %}
Client's type, `customer`, `staff` or `vendor`
{% endapi-method-parameter %}

{% api-method-parameter name="settlement\_bank" type="string" required=false %}
Client's settlement bank
{% endapi-method-parameter %}

{% api-method-parameter name="account\_number" type="string" required=false %}
Client's account number
{% endapi-method-parameter %}

{% api-method-parameter name="client\_id" type="string" required=true %}
Client ID
{% endapi-method-parameter %}

{% api-method-parameter name="due\_date" type="string" required=true %}
Invoice due date MM/DD/YYYY
{% endapi-method-parameter %}

{% api-method-parameter name="free bearer" type="string" required=true %}
Invoice fee bearer `account` or `client`
{% endapi-method-parameter %}

{% api-method-parameter name="tokenize" type="string" required=false %}
Tokenize card used to make payment for this invoice `true` or `false`, defaults to false.
{% endapi-method-parameter %}

{% api-method-parameter name="card\_token" type="string" required=false %}
Card token generated from a tokenized transaction to automatically make payment for this invoice.
{% endapi-method-parameter %}

{% api-method-parameter name="items" type="array" required=true %}
Invoice items
{% endapi-method-parameter %}

{% api-method-parameter name="item" type="string" required=true %}
Item's names
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=true %}
Item's description
{% endapi-method-parameter %}

{% api-method-parameter name="unit\_cost" type="string" required=true %}
Item's unit cost
{% endapi-method-parameter %}

{% api-method-parameter name="quantity" type="string" required=true %}
Item's quantity
{% endapi-method-parameter %}

{% api-method-parameter name="recipient" type="string" required=false %}
Invoice payment recipent `account`, or `wallet` Defaults to `account`
{% endapi-method-parameter %}

{% api-method-parameter name="recipient\_id" type="string" required=false %}
Invoice payment recipient id \(Wallet Ref.\) Required if recipient is `wallet`
{% endapi-method-parameter %}

{% api-method-parameter name="merchant\_ref" type="string" required=false %}
Merchant's unique invoice refrence code
{% endapi-method-parameter %}

{% api-method-parameter name="metadata" type="string" required=false %}
Key-value pairs object
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
curl https://api.payant.ng/invoices \
-H "Content-Type: application/json" \
-H "Authorization: Bearer SECRET_KEY" \
-d '{ "client": {
            "first_name": "Albert",
            "last_name": "Jane",
            "email": "jane@alberthospital.com",
            "phone": "+2348012345678"
        },
        "due_date": "12/30/2016",
        "fee_bearer": "client",
        "items": [
            "item": "Website Design",
            "description": "5 Pages Website plus 1 Year Web Hosting",
            "unit_cost": "50000.00",
            "quantity": "1"
        ] 
    }' \
-X POST 
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=302 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
  "status": "success",
  "message": "Invoice created successfully.",
  "data": {
    "id": 1,
    "company_id": "1",
    "client_id": "1",
    "reference_code": "j9CbiTN0oJe4vWhglyS2",
    "payment_id": null,
    "fee_bearer": "client",
    "mail_status": "unsent",
    "status": "0",
    "due_date": "1483056000",
    "created_at": "2016-12-21 18:46:30",
    "updated_at": "2016-12-21 18:46:30",
    "deleted_at": null,
    "client": {
        "id": 1
        "company_id": 1,
        "name": "Albert Specialist Hospital",
        "first_name": "Albert",
        "last_name": "Jane",
        "email": "jane@alberthospital.com",
        "phone": "+2348012345678",
        "website": "http://www.alberthospital.com",
        "address": "Wase II",
        "type": "Customer",
        "settlement_bank": "",
        "account_name": "",
        "account_number": "",
        "status": "1",
        "created_at": "2016-12-21 17:19:10",
        "updated_at": "2016-12-21 17:19:10",
        "deleted_at": null
    },
    "items": [
        {
            "id": "1",
            "company_id": "1",
            "client_id": "1",
            "name": "Website Design",
            "description": "5 Pages Website plus 1 Year Web Hosting",
            "quantity": "1",
            "unit_cost": "50000.00",
            "status": "0",
            "due_date": "1483056000",
            "created_at": "2016-12-21 17:19:10",
            "updated_at": "2016-12-21 17:19:10",
            "deleted_at": null
        }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="warning" %}
**Heads up!**

Only one of `client` or `client_id` is required per invoice. The `client` parameter will allow you to add a new customer while invoicing on the fly in case you don't have a `client_id`. Client will not be added if already exist.

For you to tokenize cards, please contact Payant Support.
{% endhint %}


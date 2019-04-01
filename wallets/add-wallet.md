# Add Wallet

{% api-method method="post" host="" path="https://api.payant.ng/wallets" %}
{% api-method-summary %}
Add Wallet
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=true %}
Wallet's name
{% endapi-method-parameter %}

{% api-method-parameter name="passcode" type="string" required=true %}
Wallet's passcode\(min of 6 char\)
{% endapi-method-parameter %}

{% api-method-parameter name="settlement\_bank" type="string" required=true %}
Wallet's settlement bank
{% endapi-method-parameter %}

{% api-method-parameter name="account\_number" type="string" required=true %}
Wallet's account number
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
curl https://api.payant.ng/wallets \
-H "Content-Type: application/json" \
-H "Authorization: Bearer SECRET_KEY" \
-d '{ "name": "John Doe Wallet",
    "passcode": "937347", 
    "settlement_bank": "000013",
    "account_number": "0123456789" }' \
-X POST 
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=302 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "status": "success",
  "message": "Wallet was added successfully.",
  "data": {
    "company_id": 1,
    "name": "John Doe Wallet",
    "balance": "0.00",
    "currency": "NGN",
    "status": "1",
    "reference_code": "PMojL342gd",
    "status": "1",
    "created_at": "2017-07-27 08:10:33",
    "updated_at": "2017-07-27 08:10:33",
    "id": 1
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


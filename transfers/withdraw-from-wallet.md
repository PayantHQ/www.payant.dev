# Single Transfer

{% api-method method="post" host="" path="https://api.payant.ng/wallets/withdraw/:reference\_code" %}
{% api-method-summary %}
Withdraw from Wallet
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
{% api-method-parameter name="settlement\_bank" type="string" required=true %}
Client's settlement bank
{% endapi-method-parameter %}

{% api-method-parameter name="account\_number" type="string" required=true %}
Client's account number
{% endapi-method-parameter %}

{% api-method-parameter name="amount" type="string" required=true %}
Amount to send
{% endapi-method-parameter %}

{% api-method-parameter name="passcode" type="string" required=true %}
Wallet's Passcode
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
curl https://api.payant.ng/wallets/withdraw/PMojL342gd \
-H "Content-Type: application/json" \
-H "Authorization: Bearer SECRET_KEY" \
-d '{ "settlement_bank": "044",
    "account_number": "0000000000",
    "amount": "1500.00",
    "passcode": "937347" }' \
-X POST 
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=302 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
  "status": "success",
  "message": "Withdrawal successful.",
  "data": { 
    "company_id": "1",
    "wallet_id": "1",
    "wallet_reference_code": "PMojL342gd",
    "currency": "NGN",
    "amount": "1500.00",
    "reference_code": "v0rX5GbWsH4FZB63tnjh",
    "type": "Withdrawal",
    "channel": "Wallet",
    "status": "1",
    "disburse_recipients": "",
    "created_at": "2016-12-21 18:50:30",
    "updated_at": "2016-12-21 18:50:30",
    "id": 2
    "transaction_date": "2017-07-26T19:50:31.000Z",
    "payment_id": "",
    "referrer": "",
    "gateway_response": "Successful",
    "disburse_status": "1",
    "disburse_ref": "TTMW000345454546",
    "disburse_response": "Successful",
    "disburse_recipients_response": "",
    "settlement_bank": "044",
    "account_number": "0000000000",
    "account_name": "Test",
}
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


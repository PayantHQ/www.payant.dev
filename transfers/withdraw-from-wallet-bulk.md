# Bulk Transfer

{% api-method method="post" host="" path="https://api.payant.ng/wallets/withdraw/:reference\_code" %}
{% api-method-summary %}

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
Recipient's settlement bank
{% endapi-method-parameter %}

{% api-method-parameter name="account\_number" type="string" required=true %}
Recipient's account number
{% endapi-method-parameter %}

{% api-method-parameter name="amount" type="string" required=true %}
Amount to send
{% endapi-method-parameter %}

{% api-method-parameter name="passcode" type="string" required=true %}
Wallet's passcode
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
curl https://api.payant.ng/wallets/withdraw/bulk/PMojL342gd \
-H "Content-Type: application/json" \
-H "Authorization: Bearer SECRET_KEY" \
-d '{ "recipients": [{
        "settlement_bank": "044",
        "account_number": "0000000000",
        "amount": "1500.00",
    },
    {
        "settlement_bank": "058",
        "account_number": "1111111111",
        "amount": "1000.00",
    }]
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
  "message": "Withdrawal queued for processing.",
  "data": { 
    "company_id": "1",
    "wallet_id": "1",
    "wallet_reference_code": "PMojL342gd",
    "currency": "NGN",
    "amount": "1500.00",
    "reference_code": "v0rX5GbWsH4FZB63tnjh",
    "type": "BulkWithdrawal",
    "channel": "Wallet",
    "status": "1",
    "disburse_recipients": "[{\"settlement_bank\":\"044\",\"account_number\":\"0000000000\",\"amount\":\"1500.00\"},{\"settlement_bank\":\"048\",\"account_number\":\"1111111111\",\"amount\":\"1000.00\"}]",
    "created_at": "2016-12-21 18:50:30",
    "updated_at": "2016-12-21 18:50:30",
    "id": 2
    "transaction_date": "2017-07-26T19:50:31.000Z",
    "payment_id": "",
    "referrer": "",
    "gateway_response": "Successful",
    "disburse_status": "1",
    "disburse_ref": "BATCH gaZbf8ULE1BwXnWzhcJq",
    "disburse_response": "Successful",
    "disburse_recipients_response": "{\"status\":\"success\",\"data\":{\"batchId\":1447,\"message\":\"Disbursement queued for processing.\"}}"
}
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


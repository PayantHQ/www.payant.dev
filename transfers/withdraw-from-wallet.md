# Single Transfer

{% api-method method="post" host="https://api.payant.ng/wallets/withdraw/:reference\_code" path="" %}
{% api-method-summary %}
Single Transfer
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="reference\_code" type="string" required=true %}
Wallet reference code
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Payant secret key prefixed by "Bearer "
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="settlement\_bank" type="string" required=true %}
6 digit bank code gotten from Get Banks
{% endapi-method-parameter %}

{% api-method-parameter name="account\_number" type="string" required=true %}
NUBAN account number
{% endapi-method-parameter %}

{% api-method-parameter name="amount" type="string" required=true %}
Amount to send
{% endapi-method-parameter %}

{% api-method-parameter name="remark" type="string" required=false %}
Wallet's Remark to show on customer bank statement
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
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

### Request

```bash
curl https://api.payant.ng/wallets/withdraw/PMojL342gd \
-H "Content-Type: application/json" \
-H "Authorization: Bearer SECRET_KEY" \
-d '{ "settlement_bank": "044",
    "account_number": "0000000000",
    "amount": "30000.00",
    "remark": "March 2017 Salary Payment" }' \
-X POST 
```

### Response

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


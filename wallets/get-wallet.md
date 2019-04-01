---
description: GET
---

# Get Wallet

**Resource**  
[https://api.payant.ng/wallets/:reference\_code](https://api.payant.ng/wallets/:reference_code)

### **Example**

```javascript
curl https://api.payant.ng/wallets/PMojL342gd \
-H "Content-Type: application/json" \
-H "Authorization: Bearer SECRET_KEY" \
-X GET 
```

### **Response**

```javascript
{
  "status": "success",
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


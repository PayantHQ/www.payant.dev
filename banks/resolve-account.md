---
description: POST
---

# Resolve Account

**Resource**  
[https://api.payant.ng/resolve-account](https://api.payant.ng/resolve-account)

### **Example**

```javascript
curl https://api.payant.ng/resolve-account \
-H "Content-Type: application/json" \
-H "Authorization: Bearer SECRET_KEY" \
-d '{ "settlement_bank": "058",
      "account_number": "0123456789" }' \
-X POST 
```

### **Response**

```javascript
{
  "status": "success",
  "message": "Account resolved successfully.",
  "data": {
    "settlement_bank": 058,
    "account_number": "01234567890",
    "account_name": "JANE, ALBERT SPECIALIST HOSPITAL"
  }
}
```


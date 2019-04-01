---
description: GET
---

# Send Invoice

**Resource**  
[https://api.payant.ng/invoices/send/:reference\_code](https://api.payant.ng/invoices/send/:reference_code)

### **Example**

```javascript
curl https://api.payant.ng/invoices/send/j9CbiTN0oJe4vWhglyS2 \
-H "Content-Type: application/json" \
-H "Authorization: Bearer SECRET_KEY" \
-X GET 
```

### **Response**

```javascript
{
  "status": "success",
  "message": "Invoice successfully sent."
  }
}
```


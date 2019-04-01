---
description: GET
---

# Disable / Enable Wallet

**Resource**  
[https://api.payant.ng/wallets/status/:reference\_code](https://api.payant.ng/wallets/status/:reference_code)

### **Example**

```java
curl https://api.payant.ng/wallets/status/PMojL342gd \
-H "Content-Type: application/json" \
-H "Authorization: Bearer SECRET_KEY" \
-X GET 
```

### **Response**

```javascript
{
  "status": "success",
  "message": "Wallet was updated successfully."
}
```




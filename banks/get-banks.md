---
description: GET
---

# Get Banks

**Resource**  
[https://api.payant.ng/banks](https://api.payant.ng/banks)

### **Example**

```javascript
curl https://api.payant.ng/banks \
-H "Content-Type: application/json" \
-H "Authorization: Bearer SECRET_KEY" \
-X GET 
```

### **Response**

```javascript
{
  "status": "success",
  "data": {
      "214": "FIRST CITY MONUMENT BANK PLC",
      "215": "UNITY BANK PLC",
      .....,
      .....,
      .....,
      "035": "WEMA BANK PLC",
      "057": "ZENITH BANK PLC"
    }
  }
}
```


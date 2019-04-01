---
description: GET
---

# Get Client



**Resource**  
[https://api.payant.ng/clients/:client\_id](https://api.payant.ng/clients/:client_id)

### **Example**

```javascript
curl https://api.payant.ng/clients/1 \
-H "Content-Type: application/json" \
-H "Authorization: Bearer SECRET_KEY" \
-X GET 
```

### **Response**

```javascript
{
  "status": "success",
  "data": {
    "id": 1,
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
  }
}
```


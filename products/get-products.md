---
description: GET
---

# Get Products

**Resource**  
[https://api.payant.ng/products](https://api.payant.ng/products)

### **Example**

```javascript
curl https://api.payant.ng/products \
-H "Content-Type: application/json" \
-H "Authorization: Bearer SECRET_KEY" \
-X GET 
```

### **Response**

```javascript
{
  "status": "success",
  "data": [
    {
        "id": 1
        "company_id": 1,
        "name": "Website Design",
        "description": "5 Pages Website plus 1 Year Web Hosting",
        "unit_cost": "50000.00",
        "type": "service",
        "image": "default.png",
        "status": "1",
        "created_at": "2016-12-21 18:46:30",
        "updated_at": "2016-12-21 18:46:30",
        "deleted_at": null
    }
  ]
}
```


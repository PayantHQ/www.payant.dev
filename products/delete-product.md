---
description: DEL
---

# Delete Product

**Resource**  
[https://api.payant.ng/products/:product\_id](https://api.payant.ng/products/:product_id)

### **Example**

```javascript
curl https://api.payant.ng/products/1 \
-H "Content-Type: application/json" \
-H "Authorization: Bearer SECRET_KEY" \
-X DELETE 
```

### **Response**

```javascript
{
  "status": "success",
  "message": "Product deleted successfully."
}
```


# Delete Invoice

**Resource**  
[https://api.payant.ng/invoices/:reference\_code](https://api.payant.ng/invoices/:reference_code)

### **Example**

```javascript
curl https://api.payant.ng/invoices/j9CbiTN0oJe4vWhglyS2 \
-H "Content-Type: application/json" \
-H "Authorization: Bearer SECRET_KEY" \
-X DELETE 
```

### **Response**

```javascript
{
  "status": "success",
  "message": "Invoice deleted successfully."
}
```


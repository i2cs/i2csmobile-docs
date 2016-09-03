#i2CSMobile : 09 Customer

This test will run API calls related to Customer controller

##09.1 api2/customer : Adds Customer when Placing an Order

Load an existing Customer to an Order or updates Customer information of an Order

> Supported Parameters

* `customer_id` [Number] Existing Customer ID to be loaded

* `firstname` [String] Customers first name. must be between 1 and 32 characters

* `lastname` [String] Customers last name. must be between 1 and 32 characters

* `email` [Email] Customers email address. must be a valid email address

* `telephone` [String] Customers telephone number. must be between 3 and 32 characters

* `customer_group_id` [Number] Customer group id. if none provided `config_customer_group_id` will be assigned


> Success Response

```
{
  "success": "You have successfully modified customers"
}
```

> Error Response

```
{
  "error": {
    "firstname": "First Name must be between 1 and 32 characters!",
    "lastname": "Last Name must be between 1 and 32 characters!",
    "email": "E-Mail Address does not appear to be valid!",
    "telephone": "Telephone must be between 3 and 32 characters!"
  }
}
```

##09.2 api2/customers/groups : Get Customer Groups

Gets a list of Customer Groups via API


> Success Response

```
{
  "customer_groups": [
    {
      "customer_group_id": "1",
      "approval": "0",
      "sort_order": "1",
      "language_id": "1",
      "name": "Default",
      "description": "test"
    }
  ]
}
```

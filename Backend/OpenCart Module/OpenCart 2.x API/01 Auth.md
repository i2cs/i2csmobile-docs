#i2CSMobile : 01 Auth [deprecate]

> *Note* No longer need this method

Authentication with i2CSMobile API. All secured API calls are needed this API call run first as it will start a valid session

##1.1 api2/login_mobile : Login

Generates a valid token for secured API calls

> Success Response

```
{
    "success":"Success: API session successfully started!",
    "token":"aPyo1uEhFQCkZ3kxxh44I51xnwTb7dRt"
}
```

> Error Response

* this error is caused by not providing a valid API Key in the OpenCart i2CSMobile admin panel. First go to `System > Users > API` and create a new API user. Generate a key and copy/paste that to `Mobile API Key` field of i2CSMobile admin panel.

```
{
  "error": {
    "key": "Warning: Incorrect API Key!"
  }
}
```

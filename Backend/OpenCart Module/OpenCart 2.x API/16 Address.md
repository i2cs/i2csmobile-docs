#i2CSMobile : 16 Address

This contains API calls related to Address

##16.1 api2/address: Get Address(s) of the Customer

Returns a list of Countries and Customer addresses. `address_id` field represents the default address id


> Success Response

```
{
  "address_id": "7",
  "countries": [
    {
      "country_id": "244",
      "name": "Aaland Islands",
      "iso_code_2": "AX",
      "iso_code_3": "ALA",
      "address_format": "",
      "postcode_required": "0",
      "status": "1"
    }
  ],
  "addresses": {
    "7": {
      "address_id": "7",
      "firstname": "Madusha",
      "lastname": "Kumarasiri",
      "company": "",
      "address_1": "Address Line 1",
      "address_2": "Address Line 2",
      "postcode": "00100",
      "city": "Colombo",
      "zone_id": "35131",
      "zone": "",
      "zone_code": "",
      "country_id": "94",
      "country": "Heard and Mc Donald Islands",
      "iso_code_2": "HM",
      "iso_code_3": "HMD",
      "address_format": "",
      "custom_field": null
    }
  },
  "country_id": "222",
  "zone_id": "254",
  "custom_fields": [],
  "payment_address_custom_field": []
}
```

##16.2 api2/address/getZones: Get Zones

Returns a list of Zones of a given Country. `country_id` field is required



> Supported Parameters

* `country_id` [Number] Country id



> Success Response

```
{
  "zones": [
    {
      "zone_id": "1388",
      "country_id": "94",
      "name": "Flat Island",
      "code": "F",
      "status": "1"
    },
    {
      "zone_id": "1391",
      "country_id": "94",
      "name": "Heard Island",
      "code": "H",
      "status": "1"
    },
    {
      "zone_id": "1389",
      "country_id": "94",
      "name": "McDonald Island",
      "code": "M",
      "status": "1"
    },
    {
      "zone_id": "1390",
      "country_id": "94",
      "name": "Shag Island",
      "code": "S",
      "status": "1"
    }
  ]
}
```

16.3 api2/address/save: Save Address

Save a new address or update an existing address. Updates if `address_id` is passed, otherwise add as a new address


> Supported Parameters

* `firstname` [String] Customers first name. must be between 1 and 32 characters

* `lastname` [String] Customers last name. must be between 1 and 32 characters

* `company` [String] Customers company name

* `address_1` [String] Address line 1. must be between 3 and 128 characters

* `address_2` [String] Address line 2

* `city` [String] Address City. must be between 2 and 128 characters

* `postcode` [String] Postal code

* `country_id` [Number] Country id

* `zone_id` [Number] Zone id

* `country_id` [Number] Country id

* `address_id` [Number] Address id


> Success Response

```
[]
```

> Error Response 401 Unauthorized

```
{
  "error": "Not logged in"
}
```
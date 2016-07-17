#i2CSMobile : 18 External Auth

Authenticate with external providers

##18.1 api2/auth/handler : Auth Handler

Starts the external authentication flow. `provider` is a required parameter. It redirects to OAuth login page of respective provider and renders a `html` page. This API call should be called within an inAppBrowser.

> Success Response

* Generates an HTML page
* On a success authentication redirects to a new URL with newly created customer/logged in customer `id`,

    `?route=api2/auth/handler/success&id=7`


> Error Response

* Shows an error in HTML format. Further more if error occurs, it redirects to a new URL,

    `?route=api2/auth/handler/error&error=Error message`

##Adding a New Language

This demonstrates how to add a new language in i2CSMobile app
----

###Introduction

Language files are located in the `www` > `languages` folder. You can find there are folders for each language currently available in the mobile app. The language folder should be named following `ISO 639-1` language code, dash, ISO country code. Ex, `en-US`. See the [complete list of language codes](http://www.w3schools.com/tags/ref_language_codes.asp) and [complete list of country codes](http://www.w3schools.com/tags/ref_country_codes.asp). Within the folder you have a set of `json` files containing key value pairs. Key represents the label name used in the app UI and value is the localized language string. 

We used an angular i18n library available on github to implement the internationalization. Refer [https://github.com/doshprompt/angular-localization](https://github.com/doshprompt/angular-localization) for more information.

Note: Language strings can not contain HTML tags, they are supposed to be clear strings. However, you can have variables in the string (see bellow).

###Create a new language pack

In this example, lets assume you are translating the app UI into `Italian`. Our language pack name will be `it-IT`. 

1.	Create a new folder, `it-IT` in `languages` folder

2.	We can use a reference language pack, so copy the content of `en-US` folder into the `it-IT` folder.

3.	Right click on the `cart.lang.json` and open it with any text editor. (ex, notepad, notepad++)
	File contains a `json` data structure with following format,
	```
	{
		'key' : 'value'
	}
	```

	Note: You can use translation softwares like `POEditor` for the translation process. Data needs to be exported back to `json` format and expected to be in same format as above.
	
4.	Translate the English content into Italian. Note that you have to make sure the `key` is unchanged while you do translations. You might notice that some language strings contains curly braces. These are used to mark `variables` within the string. You must not change any word appear inside curly braces. See the following example,
	>English
	```
	"registered_main": "Hi {firstname}, you are now registered!",
	```
	
	> French
	```
	"registered_main": "Salut {firstname}, vous êtes maintenant inscrit!",
	```

5.	Do the translation to all the language files.

###Loading the language to app

After creating the language pack, that needs to be loaded to the UI. Language switch is located in the `info` tab of the app.

1.	Go to `variables.js`

2.	There should be a `constant` with `json` array having the key `LANGUAGES`. Add following entry to the `json` array,
	```
		{ name: "Italian", language_id: "it-IT" },
	```
3.	Open app.js and edit localeSupported and localeFallbacks values
		localeSupported - list of languages currently supported
		localeFallbacks - fallbacks when a particular language is present but not for the region from which the app is being opened (e.g. en-GB will use en-US)

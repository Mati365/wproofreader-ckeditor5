WProofreader plugin for CKEditor 5
===================================

The ultimate spelling and grammar checking tool for your web app. It provides both instant and in a dialog proofreading modes in a convenient UI.
This package implements proofreader support for CKEditor 5.

![WProofreader plugin for CKEditor 5 View](https://webspellchecker.com/app/images/wproofreader_plugin_for_ckeditor5.png)

The multilingual spelling and grammar checking solution for CKEditor 5. It provides both instant and in dialog proofreading modes in a convenient UI. 
WProofreader plugin for CKEditor 5 inherits all functionality of the WProofreader component with slight adaptation to the view and features of the editor. For more details, visit the [WProofreader repo](https://github.com/WebSpellChecker/wproofreader) or [official web page](https://webspellchecker.com/wsc-proofreader/).

## Table of contents

* [Install instructions](#install-instructions)
* [Documentation](#documentation)
* [Reporting issues](#reporting-issues)
* [Technical support or questions](#technical-support-or-questions)
* [License](#license)

## Install instructions

1. Install the npm module.

	```
	npm install wproofreader-ckeditor5
	```

2. Add a new plugin and its configuration to CKEditor.

	Set the WProofreader configuration data into the `wproofreader` field of the CKEditor 5 config. All available options are described in [API docs](https://webspellchecker.com/docs/api/wscbundle/Options.html).

	For the **Cloud-based** version of WProofreader:

	```js
	import WProofreader from 'wproofreader-ckeditor5';
	...

	ClassicEditor
		.create( editorElement, {
			plugins: [ ..., WProofreader],
			wproofreader: {
				serviceId: 'your-service-ID',
				srcUrl: 'https://svc.webspellchecker.net/spellcheck31/wscbundle/wscbundle.js'
			}
		})
	```

	`serviceId` is a mandatory parameter for activating and using the plugin pointed to the Cloud-based version of WProofreader.

	For the **Server-based** version of WProofreader:

	```js
	import WProofreader from 'wproofreader-ckeditor5';
	...

	ClassicEditor
		.create( editorElement, {
			plugins: [ ..., WProofreader],
			wproofreader: {
				serviceProtocol: 'https',
				serviceHost: 'localhost',
				servicePort: '2880',
				servicePath: '/',
				srcUrl: 'https://host_name/virtual_directory/wscbundle/wscbundle.js'
			}
		})
	```

	Unlike the Cloud-based version, the `serviceId` parameter is not used here. **Instead, it is required to specify the path to the back-end hosted on the client’s end.**

## Documentation

To find out more, refer the following documentation:

* [WProofreader API documentation](https://webspellchecker.com/docs/api/wscbundle/Options.html)
* [CKEditor 5 Framework documentation](https://ckeditor.com/docs/ckeditor5/latest/framework/index.html)

## Reporting issues

We use GitHub Issues as the official public bug tracker for WProofreader. Here are some recommendations to take into account when reporting an issue:

* Provide steps which help us to reproduce an issue. A sample page or JSFiddle is always welcomed.
* Some issues may be browser and integration-specific. So, please specify what browser and integration you encountered the issue.

## Technical support or questions

Holders of an active subscription to the services or a commercial license have access to professional technical assistance directly from the support team. [Contact us here](https://webspellchecker.com/contact-us/).

## License

In order to use WProofreader plugin for CKEditor 5, you have to purchase a license accordingly. You can find more about that on our website on the [pricing plan page](https://webspellchecker.com/pricing/) or by contacting our [sales team](https://webspellchecker.com/contact-us/).

You can start with an evaluation license first and see how the product works. [Request a free trial here](https://webspellchecker.com/free-trial/).

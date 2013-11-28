SUDS WSDL module 
================

Basic usage:

```	
	var WSDL = require('wsdl');
	var wsdl = new WSDL({
		bindingHandlers: [
			function (binding, element) {
			},
			function (...
		],
		portHandlers: [
			function (port, element) { .. },
			...
		],
		operationHandlers: [
			function (operation, element) { .. },
			...
		],
		messageHandlers: [ ... ],
		portTypeHandlers: [ ... ],
		serviceHandlers: [ ... ],
		partHandlers: [ ... ]
	});
	wsdl.load(url-or-file);

	wsdl.addBindingHandler(function (binding, element) {
		...
	});
	wsdl.addPortHandler(function (port, element) {
		...
	});
	wsdl.addOperationHandler(...);
	wsdl.addMessageHandler(...);
	wsdl.addPortTypeHandler(...);
	wsdl.addServiceHandler(...);
	wsdl.addPartHandler(...);
  
	var msg = wsdl.getMessage(name);
	var port = wsdl.getPortType(name);
	var binding = wsdl.getBinding(name);
	var service = wsdl.getService(name);
```

Alternative constructor:

```
	var wsdl = new WSDL.load({ ... options as above ... }, url-or-file);
```

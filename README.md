SUDS WSDL module 
================

Basic usage:

```	
	var WSDL = require('wsdl');
	var wsdl = new WSDL({
		messageHandlers: [],
		partHandlers: [],
		portTypeHandlers: [],
		bindingHandlers: [],
		operationHandlers: [],
		serviceHandlers: [],
		portHandlers: []
	});
	wsdl.load(url-or-file);

	wsdl.addMessageHandler();
	wsdl.addPartHandler();
	wsdl.addPortTypeHandler();
	wsdl.addBindingHandler();
	wsdl.addOperationHandler();
	wsdl.addServiceHandler();
	wsdl.addPortHandler();

  
	wsdl.getMessage();
	wsdl.getPortType();
	wsdl.getBinding();
	wsdl.getService();
```

Alternative constructor:

```
	var wsdl = new WSDL.load({ ... options as above ... }, url-or-file);
```

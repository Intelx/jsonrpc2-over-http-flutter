

jsonrpc2-flutter
================
This project is a repackage of [jsonrpc2-dart](https://github.com/jwashin/jsonrpc2-dart) made to be compatible with Flutter.

The sdk has been upgraded to Dart 2 as it is now the default sdk for Flutter.

For more details please visit the [original project](https://github.com/jwashin/jsonrpc2-dart). 
 
Basic Usage
-------------

- Import the client library.
- Create a ServerProxy with the url for the desired endpoint.
- Call a method on that endpoint, error check, and do something with the result.

 
        import 'package:jsonrpc2/jsonrpc_io_client.dart';
        proxy = ServerProxy('http://example.com/some_endpoint');
        proxy.call('some_method',[arg1, arg2])
             .then((returned)=>proxy.checkError(returned))
             .then((result){do_something_with(result);})
             .catchError((error){handle(error);});

Credit
------
All credit to [jwashin](https://github.com/jwashin) for the original implementation, only minor changes were needed to ensure Flutter compatibility.




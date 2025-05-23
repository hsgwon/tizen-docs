# Common Cordova

You can handle common Cordova functionality, such as interfaces for success and error handlers.

The Cordova API is mandatory for Tizen Mobile, Wearable, and TV profiles, which means that it is supported on all mobile, wearable, and TV devices. All mandatory APIs are supported on the Tizen emulators.

The Cordova API defines a global interface, containing only 1 empty member: `cordova`. The `window` element implements the interface.

Cordova defines a common interface for success and error callbacks:

- The success callbacks have no parameters, and return no value.

- The error callbacks have 1 parameter:

  ```
  function f(error) {}
  ```

  The error callback parameter has the following properties:

  - `code`: Number representing the type of the error
  - `name`: Short text representing the type of the error
  - `message`: Text containing information about the error

> [!NOTE]
> To perform any Cordova-related operations, you must wait until Cordova is fully set up (the `deviceready` event occurs):
> ```
> document.addEventListener('deviceready', onDeviceReady, false);
>
> function onDeviceReady() {
>     console.log('Cordova features now available');
>     console.log('Connection type: ' + navigator.connection.type);
> }
> ```



## Related information
* Dependencies
  - Tizen 3.0 and Higher for Mobile
  - Tizen 3.0 and Higher for Wearable
  - Tizen 3.0 and Higher for TV
* API References
  - [Mobile](../../api/latest/device_api/mobile/tizen/cordova/cordova.html)
  - [Wearable](../../api/latest/device_api/wearable/tizen/cordova/cordova.html)
  - [TV](../../api/latest/device_api/tv/tizen/cordova/cordova.html)

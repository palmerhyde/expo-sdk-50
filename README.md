### Minimal reproducible example

Minimal repro is in the summary below. It is a vanilla install.

### Summary

Create a new vanilla project with SDK 50
` npx create-expo-app --template blank@beta`
`? What is your app named? › expo-50`
` cd expo 50`
` npx expo start`
`i` to launch iOS emulator
`a` to launch Android emulator
`j` to launch debugger

Error message - _**_Debug: No compatible apps connected. JavaScript Debugging can only be used with the Hermes engine. Learn more: https://docs.expo.dev/guides/using-hermes/**_

If I follow the same steps above with SDK 49 the debugger launches as expected.

Note on SDK 50, I I open chrome and go to http://[my ip address]:8081/json/list an empty json array is returned `[]` If I go to the same url with SDK 49 a list of devices is returned.
```
[
  {
    "id": "2-4",
    "description": "host.exp.exponent",
    "title": "Hermes React Native",
    "faviconUrl": "https://reactjs.org/favicon.ico",
    "devtoolsFrontendUrl": "devtools://devtools/bundled/js_app.html?experiments=true&v8only=true&ws=%5B%3A%3A1%5D%3A8081%2Finspector%2Fdebug%3Fdevice%3D2%26page%3D4",
    "type": "node",
    "webSocketDebuggerUrl": "ws://[::1]:8081/inspector/debug?device=2&page=4",
    "vm": "Hermes",
    "deviceName": "sdk_gphone64_arm64 - 14 - API 34"
  },
  {
    "id": "2--1",
    "description": "host.exp.exponent",
    "title": "React Native Experimental (Improved Chrome Reloads)",
    "faviconUrl": "https://reactjs.org/favicon.ico",
    "devtoolsFrontendUrl": "devtools://devtools/bundled/js_app.html?experiments=true&v8only=true&ws=%5B%3A%3A1%5D%3A8081%2Finspector%2Fdebug%3Fdevice%3D2%26page%3D-1",
    "type": "node",
    "webSocketDebuggerUrl": "ws://[::1]:8081/inspector/debug?device=2&page=-1",
    "vm": "don't use",
    "deviceName": "sdk_gphone64_arm64 - 14 - API 34"
  },
  {
    "id": "3-2",
    "description": "host.exp.Exponent",
    "title": "Reanimated Runtime",
    "faviconUrl": "https://reactjs.org/favicon.ico",
    "devtoolsFrontendUrl": "devtools://devtools/bundled/js_app.html?experiments=true&v8only=true&ws=%5B%3A%3A1%5D%3A8081%2Finspector%2Fdebug%3Fdevice%3D3%26page%3D2",
    "type": "node",
    "webSocketDebuggerUrl": "ws://[::1]:8081/inspector/debug?device=3&page=2",
    "vm": "Hermes",
    "deviceName": "iPhone 14"
  },
  {
    "id": "3-1",
    "description": "host.exp.Exponent",
    "title": "Hermes ABI49_0_0React Native",
    "faviconUrl": "https://reactjs.org/favicon.ico",
    "devtoolsFrontendUrl": "devtools://devtools/bundled/js_app.html?experiments=true&v8only=true&ws=%5B%3A%3A1%5D%3A8081%2Finspector%2Fdebug%3Fdevice%3D3%26page%3D1",
    "type": "node",
    "webSocketDebuggerUrl": "ws://[::1]:8081/inspector/debug?device=3&page=1",
    "vm": "Hermes",
    "deviceName": "iPhone 14"
  },
  {
    "id": "3--1",
    "description": "host.exp.Exponent",
    "title": "React Native Experimental (Improved Chrome Reloads)",
    "faviconUrl": "https://reactjs.org/favicon.ico",
    "devtoolsFrontendUrl": "devtools://devtools/bundled/js_app.html?experiments=true&v8only=true&ws=%5B%3A%3A1%5D%3A8081%2Finspector%2Fdebug%3Fdevice%3D3%26page%3D-1",
    "type": "node",
    "webSocketDebuggerUrl": "ws://[::1]:8081/inspector/debug?device=3&page=-1",
    "vm": "don't use",
    "deviceName": "iPhone 14"
  }
]
```



### Environment

expo-env-info 1.0.5 environment info:
    System:
      OS: macOS 13.6.2
      Shell: 3.2.57 - /bin/bash
    Binaries:
      Node: 18.18.0 - ~/.nvm/versions/node/v18.18.0/bin/node
      npm: 10.2.5 - ~/.nvm/versions/node/v18.18.0/bin/npm
    Managers:
      CocoaPods: 1.12.1 - /usr/local/bin/pod
    SDKs:
      iOS SDK:
        Platforms: DriverKit 22.4, iOS 16.4, macOS 13.3, tvOS 16.4, watchOS 9.4
    IDEs:
      Android Studio: 2023.1 AI-231.9392.1.2311.11076708
      Xcode: 14.3.1/14E300c - /usr/bin/xcodebuild
    npmPackages:
      expo: ~50.0.0-preview.4 => 50.0.0-preview.4 
      react: 18.2.0 => 18.2.0 
      react-native: 0.73.0 => 0.73.0 
    Expo Workflow: managed

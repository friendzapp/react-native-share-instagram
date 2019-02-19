# react-native-share-instagram
Share your image with the Instagram app using `Intents` (iOS & Android)

## Getting started

`$ yarn add @nickfla1/react-native-share-instagram`

## Automatic installation

`$ react-native link @nickfla1/react-native-share-instagram`


## Usage
```javascript
import RNReactNativeSharingWinstagram from 'react-native-sharing-winstagram';

RNReactNativeSharingWinstagram.shareWithInstagram(this.state.fileName, this.state.base64EncodedImageString, message => {
  if (message) alert(message)
}, error => {
  alert(error.message) // error callback for IOs only
})
```

### Troubleshouting

* Make sure you have authorised in `Info.plist` your app to communicate with the Instagram app (iOS):

```xml
<key>LSApplicationQueriesSchemes</key>
<array>
  <string>instagram</string>
</array>

<key>NSPhotoLibraryUsageDescription</key>
<string>This app requires access to the photo library to share on Instagram.</string>
```

### Advanced usage

* You can use the [rn-fetch-blob](https://github.com/joltup/rn-fetch-blob) library to download your remote image and convert it to `.base64()`

### Next steps

##### Note: This is a fork from [this](https://github.com/micabe/react-native-share-instagram) repository.

* Modernize the whole project both javascript and native
* Add type checking
* Uniform API and error handling

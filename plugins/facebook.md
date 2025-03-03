---
title: 'Facebook'
link: https://raw.githubusercontent.com/NativeScript/plugins/main/packages/facebook/README.md
---

<div style="width: 100%; padding: 1.2em 0em">
	<img alt="github logo" src="../assets/images/github/GitHub-Mark-32px.png" style="display: inline; margin: 1em 0.5em 1em 0em">
	<a href="https://github.com/NativeScript/plugins/tree/main/packages/facebook" target="_blank" noopener>Facebook</a>
</div>

# @nativescript/facebook

```cli
npm install @nativescript/facebook
```

## Prerequisites

### Android

Before you can run the project, follow the [Getting Started Guide](https://developers.facebook.com/docs/android/getting-started/) for Facebook Android SDK to set up a Facebook app. You can skip the build.gradle changes since that's taken care of by the rnpm link step above, but make sure you follow the rest of the steps such as updating `strings.xml` and `AndroidManifest.xml`.

### iOS

Follow step 3 in the [Getting Started Guide](https://developers.facebook.com/docs/ios/use-cocoapods) for Facebook SDK for iOS.

## Usage

You can also use the Login Manager with custom UI to perform Login.

```ts
import { LoginManager, AccessToken } from '@nativescript/facebook'

LoginManager.init() // call init early in the app lifecycle e.g main.ts/app.ts

try {
  const result = await LoginManager.logInWithPermissions(['public_profile']) // LoginResult
  const accessToken = AccessToken.currentAccessToken()
} catch (e) {}

LoginManager.logOut() // Whenever you're done
```

## License

Apache License Version 2.0

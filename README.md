<a href="https://labs.moduscreate.com"><img src="https://res.cloudinary.com/modus-labs/image/upload/v1535020117/labs/logo-beep.svg" width="260" alt="Beep" /></a>
staffposition, schoolyear, name, writer, jobtitle, sno_deck
Asking for a friend
<p>
<a href="https://beep.modus.app"><img src="./src/images/pwa-badge.svg" height="40" alt="Launch Progressive Web App" /></a>
<a href="https://itunes.apple.com/us/app/beep-account-security-scanner/id1434675665?ls=1&mt=8"><img src="./src/images/app-store-badge.svg" height="40" alt="Download Beep on the App Store"/></a>
<a href="https://play.google.com/store/apps/details?id=app.modus.beep"><img src="./src/images/google-play-badge.png" height="40" alt="Get Beep on Google Play" /></a>
</p>

<hr />

## **Beep**: mobile account vulnerability scanner

Every day, over 4 million online data records are stolen or lost. Beep tells you if your online accounts have been stolen in any of these data breaches. Just enter your email address, username, or password, and we’ll tell you if it's been hacked.

## Pioneering Vue.js as a New Backend for Ionic

Beep is one of the first apps built on Vue.JS and Ionic Framework. With this combination, PHP developers no longer have to struggle with Angular to build cross platform Ionic apps. We even built our own router.

- [How it works](#how-it-works)
- [Installing](#installing)
- [Developing](#developing)
  - [Prerequisites](#prerequisites)
  - [iOS build](#ios-build)
  - [Android build](#android-build)
  - [Deploying](#deploying)
- [Ionic Vue](#ionic-vue)
- [Theming](#theming)
- [Modus Create](#modus-create)
- [License](#license)

# How it works

We've made sure that Beep won't end up yet another name on the list of data breaches. How? We hash all of your passwords and account information. In other words, we never store your passwords in plain text. Instead, we transform your password into a really, really long code and then, we send only the first five characters of that code to a server.

[![Beep Screenshot](https://res.cloudinary.com/modus-labs/image/upload/w_130,f_auto,dpr_auto/v1538144594/beep/Beep-Screenshot-iPhoneX-01.png)](https://res.cloudinary.com/modus-labs/image/upload/v1538144594/beep/Beep-Screenshot-iPhoneX-01.png)
[![Beep Screenshot](https://res.cloudinary.com/modus-labs/image/upload/w_130,f_auto,dpr_auto/v1538144594/beep/Beep-Screenshot-iPhoneX-02.png)](https://res.cloudinary.com/modus-labs/image/upload/v1538144594/beep/Beep-Screenshot-iPhoneX-02.png)
[![Beep Screenshot](https://res.cloudinary.com/modus-labs/image/upload/w_130,f_auto,dpr_auto/v1538144594/beep/Beep-Screenshot-iPhoneX-03.png)](https://res.cloudinary.com/modus-labs/image/upload/v1538144594/beep/Beep-Screenshot-iPhoneX-03.png)
[![Beep Screenshot](https://res.cloudinary.com/modus-labs/image/upload/w_130,f_auto,dpr_auto/v1538144594/beep/Beep-Screenshot-iPhoneX-04.png)](https://res.cloudinary.com/modus-labs/image/upload/v1538144594/beep/Beep-Screenshot-iPhoneX-04.png)
[![Beep Screenshot](https://res.cloudinary.com/modus-labs/image/upload/w_130,f_auto,dpr_auto/v1538144594/beep/Beep-Screenshot-iPhoneX-05.png)](https://res.cloudinary.com/modus-labs/image/upload/v1538144594/beep/Beep-Screenshot-iPhoneX-05.png)
[![Beep Screenshot](https://res.cloudinary.com/modus-labs/image/upload/w_130,f_auto,dpr_auto/v1538144594/beep/Beep-Screenshot-iPhoneX-06.png)](https://res.cloudinary.com/modus-labs/image/upload/v1538144594/beep/Beep-Screenshot-iPhoneX-06.png)

# Installing

Once you clone this repo go into the terminal and install dependencies.

```shell
npm install
```

Now you're ready to serve the development build.

```sh
npm run serve
```

# Developing

Beep is built with amazing libraries

- [Ionic](https://github.com/ionic-team/ionic)
- [Vue](https://github.com/vuejs/vue)
- [Ionic-Vue](https://github.com/ModusCreateOrg/ionic-vue)
- [Capacitor](https://github.com/ionic-team/capacitor)
- [Webpack](https://github.com/webpack/webpack)

## Prerequisites

Node 8.x+ is required for development.

## iOS build

Make sure you have `cocoapods` on your Mac OS. You can install `cocoapods` with `gem`

```sh
sudo gem install cocoapods
```

You can create an iOS-specific build by executing:

```sh
npm run build-ios
```

## Android build

You will need [Android SDK](https://developer.android.com/studio/).

The easiest way to set it up on a Mac is with `homebrew`.

```sh
brew install android-sdk
```

On Linux you can either use your distribution's package manager

```sh
sudo apt-get install android-sdk
```

Or install via
[Flatpak](https://flathub.org/apps/details/com.google.AndroidStudio) or
[Snap](https://uappexplorer.com/snap/ubuntu/android-studio)

After the SDK is setup you can create an Android-specific build by executing:

```sh
npm run build-android
```

To create a production or debug APK you will need to [sign your app](https://developer.android.com/studio/publish/app-signing).
For a local debug build we have provided an example file

```sh
mv android/signing/keystore.properties.example android/signing/keystore.properties
```

This will rename the example file and allow you to proceed with the build process.

You may need to adjust the value of `storeFile` according to your platform

```sh
storeFile=~/.android/debug.keystore
```

## Deploying

To prepare your assets for a production deployment execute:

```sh
npm run build
```

This will create files and assets in the `dist/` directory

# Ionic Vue

<img src="https://res.cloudinary.com/modus-labs/image/upload/w_560/v1535019553/labs/logo-ionic-vue.svg"
width="260"
alt="@modus/ionic-vue">

[Ionic Vue](https://github.com/ModusCreateOrg/ionic-vue) enables Vue apps to use Ionic 4 with little to no configuration and no changes to familiar approaches. Originally a [Modus Labs](https://labs.moduscreate.com) project, Ionic Vue became part of the Ionic framework as the official support for Vue.

# Theming

For minor customizations you can edit the supplied `.env` file which allows you to edit the App name and status-bar colors for mobile/PWA builds.

Modifications of colors, fonts and other parts of UI are done in
`src/theme/common.css` and
`.vue` files in `src/components/` and `src/views/` which specify scoped styling rules.

For making modifications to native iOS and Android builds you will have to make changes within `android/` and `ios/` directories.

An in-depth description is provided by Capacitor's documentation

[Configuring iOS](https://capacitor.ionicframework.com/docs/ios/configuration)

[Configuring Android](https://capacitor.ionicframework.com/docs/android/configuration)

# Tests

To run the test suite execute:

```sh
npm test
```

This will confirm that any changes made to the original code did not break any existing functionality.

To extend the test suite create a new file in `tests/unit/` such as `new-feature.spec.js`

# Linting

Code linting is done with
[ESLint](https://github.com/eslint/eslint) and
[Prettier](https://github.com/prettier/prettier)

To run a check the project for any lint errors execute:

```sh
npm run lint
```

# Modus Create

[Modus Create](https://moduscreate.com) is a digital product consultancy. We use a distributed team of the best talent in the world to offer a full suite of digital product design-build services; ranging from consumer facing apps, to digital migration, to agile development training, and business transformation.

[![Modus Create](https://res.cloudinary.com/modus-labs/image/upload/h_80/v1533109874/modus/logo-long-black.png)](https://moduscreate.com)

This project is part of [Modus Labs](https://labs.moduscreate.com).

[![Modus Labs](https://res.cloudinary.com/modus-labs/image/upload/h_80/v1531492623/labs/logo-black.png)](https://labs.moduscreate.com)

# Licensing

This project is [MIT licensed](./LICENSE).

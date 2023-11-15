# 🚨 Breaking Changes 🚨

## General
- Raise minimum Node.js requirement to 18.x
- Breaking - Bump minimum Node version from 16 to 18 [facebook/react-native#37709](https://github.com/facebook/react-native/pull/37709)
- TypeScript 5.0 upgrade
- Bump TypeScript in template from 4.8.4 to 5.0.4 [facebook/react-native#36862](https://github.com/facebook/react-native/pull/36862)

## Android
- Major bump of Fresco to 3.0.0
- Fresco to 3.0.0 [facebook/react-native#38275](https://github.com/facebook/react-native/pull/38275)
- Bump to AGP 8.0
- Upcoming changes for libraries in React Native 0.73 [react-native-community/discussions-and-proposals#671](https://github.com/react-native-community/discussions-and-proposals/issues/671)
- Breaking changes for libraries -> [Android Developers](https://developer.android.com/build/releases/gradle-plugin#namespace-dsl)
- AGP to 8.0.2 [facebook/react-native#37019](https://github.com/facebook/react-native/pull/37019)

## iOS
- Metro will no longer be automatically started when running builds via Xcode
- Remove run Metro hook from Xcode build, remove launchPackager scripts [facebook/react-native#38242](https://github.com/facebook/react-native/pull/38242)
- Raise minimum iOS version to 13.4
- Move min ios version to 13.4 for OSS [facebook/react-native#36795](https://github.com/facebook/react-native/pull/36795)

# 📚 Detailed Explanation 📚

## 🎉 DevX Improvements

### Metro
- 0.73 will be offering stable symlink support and enabled by default
- Closing the #1 issue in Metro
- Out-of-the-box support for common monorepo layouts in react native projects
- Babel preset and transformer moved to react native from Metro (faster builds and smaller bundles)
- New configuring metro docs. [https://reactnative.dev/docs/metro]
- Support for metro.config.cjs
- Revamped Metro's File Map Cache for improvement in startup speed

### Debugging
- New Debugger Frontend
  - One-click debug flow (front end replacing flipper)
  - Workflow is zero install (works with either Google Chrome or Microsoft Edge installed on system)
  - Can be triggered by using 'j' as hotkey
  - It is based on chrome dev tools

### Hermes
- Background console logs (collects all the logs in absence of debugger in development mode)
- Once the debugger is triggered buffered logs are sent (just like web)

### Docs
- Refactoring of debugging docs and addition of new features

### Flipper
- No longer the default debugging experience starting 0.73
- In 0.74, new projects will not include Flipper's native integration code
- Flipper will remain available as a standalone project

## 📱 Platform Updates

### Android
- AGP: 8.0.2 --> 8.1.0
- JDK: 11 --> 17
- Bump NDK: 24 --> 25
- Bump Fresco: 2.5.0 --> 3.0.0

### iOS
- iOS Min Version: 12.4 --> 13.4

## 🎯 Kotlin Template
- 30% of space in the code size

## 🚀 React Native Runtime
- New component that replaces the Bridge that communicates back and forth to JS and Native code

## 🌉 Interlop Layers
- [Experimental] proxy for the bridge in the new architecture

## 📝 View Configs Updates
- Old Architecture -> consists of View and View Manager
- New Architecture -> replacing view manager with static view configs (Codegen will write them for you)

## 🧪 E2E testing solution powered by CI using webdriver, appium and jest (by CallStack and Microsoft)
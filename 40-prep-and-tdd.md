# Read40: React Native
* getting started with react native .
* react native .
* expo .
* ejecting .

### *getting started with react native*

- React Native is an open source framework for building Android and iOS applications using React and the app platform’s native capabilities. With 
React Native, you use JavaScript to access your platform’s APIs as well as to describe the appearance and behavior of your UI using React 
components: bundles of reusable, nestable code. You can learn more about React in the next section. But first, let’s cover how components work in 
React Native.

- Function Components and Class Components

With React, you can make components using either classes or functions. Originally, class components were the only components that could have 
state. But since the introduction of React's Hooks API, you can add state and more to function components.

For more details see [getting started with react native](https://reactnative.dev/docs/getting-started).

### *react native*

- Create native apps for Android and iOS using React
React Native combines the best parts of native development with React, a best-in-class JavaScript library for building user interfaces.

- Use a little—or a lot. You can use React Native today in your existing Android and iOS projects or you can create a whole new app from scratch.

- Written in JavaScript—rendered with native code React primitives render to native platform UI, meaning your app uses the same native platform APIs other apps do.

- Many platforms, one React. Create platform-specific versions of components so a single codebase can share code across platforms. With React Native, one team can maintain two platforms and share a common technology—React.

- Native Development For Everyone React Native lets you create truly native apps and doesn't compromise your users' experiences. It provides a core set of platform agnostic native components like View, Text, and Image that map directly to the platform’s native UI building blocks.

![native](https://d33wubrfki0l68.cloudfront.net/7e97b18b02060f1d4b65a5850b49e2488da391bb/d60ff/img/homepage/dissection/3.png)

For more details see  [react native](https://reactnative.dev/).

### *expo*

- There are two tools that you need to develop apps with Expo: a command line app called Expo CLI to initialize and serve your project and a mobile client app called Expo Go to open it on iOS and Android. Any web browser will work for opening the project on the web.

1. Expo CLI

Expo CLI is a command line app that is the main interface between a developer and Expo tools. Expo CLI also has a web-based GUI that pops up in 
your web browser when you start your project — you can use the GUI instead of the command line interface if you're not yet comfortable using a 
terminal or prefer GUIs, both have similar capabilities.

Installing Expo CLI

                 npm install --global expo-cli

2. Expo Go app for iOS and Android

The fastest way to get up and running is to use the Expo Go app on your iOS or Android device. Expo Go allows you to open up apps that are being served through Expo CLI.

For more details see  [expo](https://expo.dev/).

### *ejecting*

1. Install Expo CLI

If you don't have it, run npm install -g expo-cli to get our command line library.
If you haven't used Expo CLI with an Expo account before, the eject command will ask you to create one.

2. Make sure you have the necessary configuration options in app.json

Ejecting requires the same configuration options as building a standalone app.

3. Eject
From your project directory, run expo eject. This will download the required dependencies and build native projects under the ios and android directories.

4. Set up and Run your native project

5. Make native changes

You can do whatever you want in the Xcode and Android Studio projects.
To add third-party native modules for React Native, non-Expo-specific instructions such as react-native link should be supported.

6. Distribute your app

For more details see  [ejecting](https://docs.expo.dev/expokit/eject/?redirected).
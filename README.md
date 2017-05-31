# React Native Navigation + MobX (w/ Provider) Boilerplate 👽

A simple boilerplate based on MobX (w/ Provider) instead of Redux and [wix/react-native-navigation](https://github.com/wix/react-native-navigation).

##### What's inside
- Tab Based App.
- Drawer. [for iOS] It supports `.push({...})`s for the first tab through MobX: `Stores.App.rootNavigator.push({...})`. You can change `.rootNavigator` in any component. (based on [this issue](https://github.com/wix/react-native-navigation/issues/1143))
- Simple auth flow. For example, If you are not logged in (see `Account` store), the app opens a modal with text inputs.
- `MobX Provider`. Now all components can use `@inject('App', 'Counter', ...)` for accessing stores through `const { App, Counter } = this.props;`. (based on [this comment](https://github.com/wix/react-native-navigation/issues/187#issuecomment-265946012)).
- In a new version, structure of the project is more organized 👌

##### What's in package.json
- `react '16.0.0-alpha.6'`
- `react-native '0.44'`
- `react-native-navigation '1.1.79'`
- `mobx '^3.1.10'`
- `mobx-react '^4.1.8'`
- `mobx-persist '^0.3.3',`

# Installation
1. Clone this repo: `git clone https://github.com/kanzitelli/react-native-navigation-mobx-boilerplate.git`
2. Install node modules: `cd react-native-navigation-mobx-boilerplate && npm i -S`
3. Rename application using [react-native-rename](https://github.com/junedomingo/react-native-rename) if needed.
4. `react-native run-ios` or `react-native run-android` (and remove the ios/build directory).
5. Enjoy :)

Thanks to [@megahertz](https://github.com/megahertz) for sharing the [gist](https://github.com/wix/react-native-navigation/issues/187#issuecomment-265946012) that shows how to create a mobx Provider which can be used with RNN.

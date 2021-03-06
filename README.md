#### ‼️ There are no major updates planned for `tui.virtual-keyboard` in the future. It will only get bug fixes.

# TOAST UI Component : Virtual Keyboard
> Component that creates a virtual keyboard that replacing the native keyboard of the browser.

[![GitHub release](https://img.shields.io/github/release/nhn/tui.virtual-keyboard.svg)](https://github.com/nhn/tui.virtual-keyboard/releases/latest)
[![npm](https://img.shields.io/npm/v/tui-virtual-keyboard.svg)](https://www.npmjs.com/package/tui-virtual-keyboard)
[![GitHub license](https://img.shields.io/github/license/nhn/tui.virtual-keyboard.svg)](https://github.com/nhn/tui.virtual-keyboard/blob/production/LICENSE)
[![PRs welcome](https://img.shields.io/badge/PRs-welcome-ff69b4.svg)](https://github.com/nhn/tui.project-name/labels/help%20wanted)
[![code with hearth by NHN](https://img.shields.io/badge/%3C%2F%3E%20with%20%E2%99%A5%20by-NHN-ff1414.svg)](https://github.com/nhn)


## 🚩 Table of Contents
* [Collect statistics on the use of open source](#Collect-statistics-on-the-use-of-open-source)
* [Browser Support](#-browser-support)
* [Features](#-features)
* [Examples](#-examples)
* [Install](#-install)
    * [Via Package Manager](#via-package-manager)
    * [Via Contents Delivery Network (CDN)](#via-contents-delivery-network-cdn)
    * [Download Source Files](#download-source-files)
* [Usage](#-usage)
    * [HTML](#html)
    * [JavaScript](#javascript)
* [Pull Request Steps](#-pull-request-steps)
    * [Setup](#setup)
    * [Develop](#develop)
    * [Pull Request Steps](#pull-request)
* [Documents](#-documents)
* [Contributing](#-contributing)
* [Dependency](#-dependency)
* [License](#-license)

## Collect statistics on the use of open source
 TOAST UI VirtualKeyboard applies Google Analytics (GA) to collect statistics on the use of open source, in order to identify how widely TOAST UI VirtualKeyboard is used throughout the world.
It also serves as important index to determine the future course of projects.
`location.hostname` (e.g. > “ui.toast.com") is to be collected and the sole purpose is nothing but to measure statistics on the usage.
 To disable GA, use the following `usageStatistics` option when creating the instance.
 ```js
var options = {
    ...
    usageStatistics: false
}
var instance = new VirtualKeyboard(container, options);
```

Or, include [`tui-code-snippet`](https://github.com/nhn/tui.code-snippet)(**v1.5.0** or **later**) and then immediately write the options as follows:

```js
tui.usageStatistics = false;
```


## 🌏 Browser Support
| <img src="https://user-images.githubusercontent.com/1215767/34348387-a2e64588-ea4d-11e7-8267-a43365103afe.png" alt="Chrome" width="16px" height="16px" /> Chrome | <img src="https://user-images.githubusercontent.com/1215767/34348590-250b3ca2-ea4f-11e7-9efb-da953359321f.png" alt="IE" width="16px" height="16px" /> Internet Explorer | <img src="https://user-images.githubusercontent.com/1215767/34348380-93e77ae8-ea4d-11e7-8696-9a989ddbbbf5.png" alt="Edge" width="16px" height="16px" /> Edge | <img src="https://user-images.githubusercontent.com/1215767/34348394-a981f892-ea4d-11e7-9156-d128d58386b9.png" alt="Safari" width="16px" height="16px" /> Safari | <img src="https://user-images.githubusercontent.com/1215767/34348383-9e7ed492-ea4d-11e7-910c-03b39d52f496.png" alt="Firefox" width="16px" height="16px" /> Firefox |
| :---------: | :---------: | :---------: | :---------: | :---------: |
| Yes | 8+ | Yes | Yes | Yes |


## 🎨 Features
* Changes the key to english, korean, number, and symbol.
* Shuffles the keys.
* Supports callback functions for each key event.
* Supports mobile devices using touch events.
* Supoorts templates.


## 🐾 Examples
* [Basic](https://nhn.github.io/tui.virtual-keyboard/latest/tutorial-example01-basic) : Example of using default options.
* [Mobile UI](https://nhn.github.io/tui.virtual-keyboard/latest/tutorial-example02-mobile-ui) : Example of the keyboard UI when used on a mobile device.


## 💾 Install

TOAST UI products can be used by using the package manager or downloading the source directly.
However, we highly recommend using the package manager.

### Via Package Manager

TOAST UI products are registered in two package managers, [npm](https://www.npmjs.com/) and [bower](https://bower.io/).
You can conveniently install it using the commands provided by each package manager.
When using npm, be sure to use it in the environment [Node.js](https://nodejs.org/ko/) is installed.

#### npm

``` sh
$ npm install --save tui-virtual-keyboard # Latest version
$ npm install --save tui-virtual-keyboard@<version> # Specific version
```

#### bower

``` sh
$ bower install tui-virtual-keyboard # Latest version
$ bower install tui-virtual-keyboard#<tag> # Specific version
```

### Via Contents Delivery Network (CDN)
TOAST UI products are available over a CDN powered by [TOAST Cloud](https://www.toast.com).

You can use CDN as below.

```html
<script src="https://uicdn.toast.com/tui.virtual-keyboard/latest/tui-virtual-keyboard.js"></script>
```

If you want to use a specific version, use the tag name instead of `latest` in the url's path.

The CDN directory has the following structure.


```
tui.virtual-keyboard/
├─ latest
│  ├─ tui-virtual-keyboard.js
│  ├─ tui-virtual-keyboard.min.js
├─ v2.0.1/
│  ├─ ...
```

### Download Source Files
* [Download bundle files](https://github.com/nhn/tui.virtual-keyboard/tree/production/dist)
* [Download all sources for each version](https://github.com/nhn/tui.virtual-keyboard/releases)


## 🔨 Usage

### HTML

Add the container element to create the component.

``` html
<ul id="tui-virtual-keyboard-container"></ul>
```

### JavaScript

This can be used by creating an instance with the constructor function.
To get the constructor function, you should import the module using one of the following ways depending on your environment.

#### Using namespace in browser environment
``` javascript
var VirtualKeyboard = tui.VirtualKeyboard;
```

#### Using module format in node environment
``` javascript
var VirtualKeyboard = require('tui-virtual-keyboard'); /* CommonJS */
```

``` javascript
import VirtualKeyboard from 'tui-virtual-keyboard'; /* ES6 */
```

You can create an instance with [options](https://nhn.github.io/tui.virtual-keyboard/latest/VirtualKeyboard) and call various APIs after creating an instance.

``` javascript
var container = document.getElementById('tui-virtual-keyboard-container');
var instance = new VirtualKeyboard(container, { ... });

instance.shuffle();
```

For more information about the API, please see [here](https://nhn.github.io/tui.virtual-keyboard/latest/VirtualKeyboard).


## 🔧 Pull Request Steps

TOAST UI products are open source, so you can create a pull request(PR) after you fix issues.
Run npm scripts and develop yourself with the following process.

### Setup

Fork `develop` branch into your personal repository.
Clone it to local computer. Install node modules.
Before starting development, you should check to haveany errors.

``` sh
$ git clone https://github.com/{your-personal-repo}/tui.virtual-keyboard.git
$ cd tui.virtual-keyboard
$ npm install
$ npm run test
```

### Develop

Let's start development!
You can see your code is reflected as soon as you saving the codes by running a server.
Don't miss adding test cases and then make green rights.

#### Run webpack-dev-server

``` sh
$ npm run serve
$ npm run serve:ie8 # Run on Internet Explorer 8
```

#### Run karma test

``` sh
$ npm run test
```

### Pull Request

Before PR, check to test lastly and then check any errors.
If it has no error, commit and then push it!

For more information on PR's step, please see links of Contributing section.


## 📙 Documents
* [Getting Started](https://github.com/nhn/tui.virtual-keyboard/blob/production/docs/getting-started.md)
* [Tutorials](https://github.com/nhn/tui.virtual-keyboard/tree/production/docs)
* [APIs](https://nhn.github.io/tui.virtual-keyboard/latest)

You can also see the older versions of API page on the [releases page](https://github.com/nhn/tui.virtual-keyboard/releases).


## 💬 Contributing
* [Code of Conduct](https://github.com/nhn/tui.virtual-keyboard/blob/production/CODE_OF_CONDUCT.md)
* [Contributing guideline](https://github.com/nhn/tui.virtual-keyboard/blob/production/CONTRIBUTING.md)
* [Issue guideline](https://github.com/nhn/tui.virtual-keyboard/blob/production/docs/ISSUE_TEMPLATE.md)
* [Commit convention](https://github.com/nhn/tui.virtual-keyboard/blob/production/docs/COMMIT_MESSAGE_CONVENTION.md)


## 🔩 Dependency
* [tui-code-snippet](https://github.com/nhn/tui.code-snippet) >=1.5.0
* [jquery](https://jquery.com/) >=1.11.0


## 📜 License

This software is licensed under the [MIT](https://github.com/nhn/tui.virtual-keyboard/blob/production/LICENSE) © [NHN](https://github.com/nhn).

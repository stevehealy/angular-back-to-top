# angular-back-to-top
**UPDATED for Angular 8**

Angular 8 component that lets the user return to the top of the screen, using a Material Design button

## Description
A spin-off of https://github.com/annapogorelova/ng2-go-top-button (full credit here for the actual back-to-top logic).
The following changes/additions were made:
* This is a working Angular v8 sample project that can be run locally
* Back-to-top logic contained within a reusable component
...Unused code stripped away and refactored for component-use.
* [Material Design FAB button] used for component

[Material Design FAB button]: https://material.io/design/components/buttons-floating-action-button.html

## Installation and Running a dev server
Clone this repo and run `npm install` to install necessary packages.
Next, run `ng serve` to start the application.
Then in your browser, go to `http://localhost:4200/`

Once the page has loaded, simply scroll down the page and the back-to-top button will appear in the bottom-right corner. Click this button to return to the top of the page. Simple!

## Usage
Import statement:
```
import { BackToTopComponent } from './components/back-to-top.component';
```

Add it to imports in your module declaration.
```
@NgModule({
    ...
    imports: [..., BackToTopComponent],
    ...
```

In your template add `<app-back-to-top></app-back-to-top>`. This will add a simple button with default styles and without animated scroll.

Example of customization:
```
<app-back-to-top [acceleration]="1" [animate]="true" [scrollDistance]="200" [speed]="40">
</app-back-to-top>
```

## Component Parameters
| Property | Type | Description |
| ------ | ------ | ------ |
| scrollDistance | *number* | Number of pixels to be scrolled Y for button to be shown. Must be greater than zero. |
| animate | *boolean* | If true, scrolling will be animated. False by default. |
| speed | *number* | Speed of animated scroll. Must be greater than 1. |
| acceleration  | *number* | Number of pixels to speed up when scrolling is animated. Zero by default - which means page will scroll with constant speed. |

## Browser Compatibility:
This project should be compatible with all browsers including IE, due to inclusion of the `web-animations-js` polyfill (See polyfills.js).

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).

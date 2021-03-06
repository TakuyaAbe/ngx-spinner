<p align="center">
  <img height="200px" width="200px" style="text-align: center;" src="https://cdn.rawgit.com/Napster2210/ngx-spinner/gh-pages/assets/logo.png">
  <h1 align="center">NgxSpinner</h1>
</p>

A library for loading spinner specifically for Angular 2/4/5. (https://napster2210.github.io/ngx-spinner/)

[![ng5](https://img.shields.io/travis/rust-lang/rust.svg?style=flat-square)]()
[![Support](https://img.shields.io/badge/Support-Angular%202%2B-brightgreen.svg?style=flat-square)]()
[![License](https://img.shields.io/npm/l/express.svg?style=flat-square)]()
[![devDependency Status](https://img.shields.io/david/expressjs/express.svg?style=flat-square)]()

The version 1.x supports supports Angular >= 5.

## Table of contents

- [Browser Support](#browser-support)
- [Demo](#demo)
- [Installation](#installation)
- [Usage](#usage)
- [Versioning](#versioning)
- [Creator](#creator)
- [Future Plan](#future-plan)
- [Credits](#credits)
- [License](#license)

## Browser Support

![Chrome](http://icons.iconarchive.com/icons/google/chrome/48/Google-Chrome-icon.png) | ![Firefox](https://support.cdn.mozilla.net/static/sumo/img/favicon.ico) | ![IE](https://www.msccruises.co.uk/wcsstore/MSCB2CStoreFrontAssetStore//images/icon_ie.png) | ![Safari](https://aplweb.sercomtel.com.br/sistemas/areaCliente/img/logoSafari.png) | ![Opera](https://www.webcomponents.org/assets/opera.png)
--- | --- | --- | --- | --- |
Latest ✔ | Latest ✔ | 10+ ✔ | Latest ✔ | Latest ✔ |

## Demo

[Working Demo](https://napster2210.github.io/ngx-spinner/)

## Installation

`ngx-spinner` is available via [npm](https://www.npmjs.com/package/ngx-spinner) and [yarn](https://yarnpkg.com/en/package/ngx-spinner)

Using npm:
```bash
$ npm install ngx-spinner --save
```

Using yarn:
```bash
$ yarn add ngx-spinner
```

## Usage

Import `NgxSpinnerModule` in  in the root module(`AppModule`):
```typescript
// Import library module
import { NgxSpinnerModule } from 'ngx-spinner';

@NgModule({
  imports: [
    // ...
    NgxSpinnerModule
  ]
})
export class AppModule { }
```

Add `NgxSpinnerService` service wherever you want to use the `ngx-spinner`.
```typescript
import { NgxSpinnerService } from 'ngx-spinner';

class AppComponent implements OnInit {
  constructor(private spinner: NgxSpinnerService) { }

  ngOnInit() {
    /** spinner starts on init */
    this.spinner.show();

    setTimeout(() => {
        /** spinner ends after 5 seconds */
        this.spinner.hide();
    }, 5000);
  }
}
```

Now use in your template
```html
<ngx-spinner></ngx-spinner>
```
See [Demo](https://napster2210.github.io/ngx-spinner/)

## NgxSpinner Service

- `NgxSpinnerService.show()`  Shows the spinner
- `NgxSpinnerService.hide()`  Hides the spinner

## NgxSpinner Component

```html
<ngx-spinner [bdOpacity]="0.9" [bdColor]="#909090" [size]="medium" [color]="#fff" [loadingText]="Loading..." [type]="ball-scale-multiple"></ngx-spinner>
```

- **[bdOpacity]**: between `0.0` to `1.0`.
  To set opacity of backdrop, default `0.8`
- **[bdColor]**: Any css color format.
  To set background-color for backdrop, default `#333`
- **[size]**: Anyone from `small`, `default`, `medium`, `large`.
  To set size of spinner, default `large`
- **[color]**: Any css color format.
  To set color of spinner, default `#fff`
- **[loadingText]**: Loading Text.
  To set loadingText of spinner, default `false`  
- **[type]**: Choose any animation spinner from [Load Awesome](http://github.danielcardoso.net/load-awesome/animations.html).
  To set type of spinner, default `ball-scale-multiple`
  
### How to use type?

- Go to the [Load Awesome](http://github.danielcardoso.net/load-awesome/animations.html).
- Select any animation, copy name of animation, replace all spaces with hyphen(-) and all letters should be lowercase. 
  - Let's say if I select "Ball 8bits" animation then `type` will be `ball-8bits`.
  - For more information you can check it out [Demo](https://napster2210.github.io/ngx-spinner/)


## Versioning

ngx-spinner will be maintained under the Semantic Versioning guidelines.
Releases will be numbered with the following format:

`<major>.<minor>.<patch>`

For more information on SemVer, please visit http://semver.org.

## Creator

#### [Yuvraj Chauhan](mailto:yuvrajchauhan3113@gmail.com)
- [@GitHub](https://github.com/Napster2210)

## Future Plan

- Interceptor Implementation (Coming soon)
- Spinner in specific container(DOM Element)

## Credits

 Inspired by [Load Awesome by Daniel Cardoso.](https://github.com/danielcardoso/load-awesome)

## License

#### The MIT License (MIT)
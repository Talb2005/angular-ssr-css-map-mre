# CssMapMre

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 18.1.1.

## Issue Description

When using style sourcemaps, with an empty path route ({path: ''}), the .css.map files are being fetched from the wrong URL path.

## Issue Reproduction

1. Clone this repository.
2. `npm install`
3. `npm run watch`
4. `npm run serve:ssr:css-map-mre` (from new terminal).
5. Open browser and navigate to http://localhost:4000.
6. Open the deveoplers console so that the .css.map files would be requested by the browser.
7. Click "About" to navigate to the About page.
8. Reload the page.
9. Click "Home" to navigate to the Home page.
10. An error will be logged in the server:
    **ERROR RuntimeError: NG04002: Cannot match any routes. URL Segment: 'about/home.component.css.map'**

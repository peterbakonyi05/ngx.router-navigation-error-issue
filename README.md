# Ngx.RouterBlankScreenIssue

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 1.5.0.

## How to replicate the issue?

Usual `npm i` and `npm start` then open http://localhost:4200

Click on the profile link and then on the home link. Home page will not load because there is an error in `ProfileComponent.ngOnDestroy`.


## Why is it a problem?
If you are using a third-party library and it throws an error during clean up, the screen will be blank. Ideally an error in `ngOnDestroy` should
not stop the router from loading the new page.

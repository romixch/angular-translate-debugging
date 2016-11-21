# angular-translate-debugging

## Why I created this repo
I recently had to build an AngularJS app which automatically detects the
language of the browser and apply the correct language. Unfortunately the
features which are provided by https://github.com/angular-translate/angular-translate
were not sufficient. It has following flaws:

- It does only consider the first language in the array `window.navigator.languages`. This is not what I was looking for. I would like to have all those languages tested before using the fallback.
- It has some problems with upper and lower cases. Let's say you register the languages `de-CH` and `fr-CH`. Then you call `$translate.use('de-ch')`. Angular translate will resolve the promise successfully but fails at translating your site. This happens for example if you use an iPhones Safari.

## What this repo does

There are two files:

- index.html: Shows you the content of different language settings accessible from your browsers JavaScript engine.
- angular.html: Contains my current approach to work around the mentioned issues.

## Cool! Did you deploy those two files somewhere

Oh, glad you asked! :-)

Try this:

- http://odiee.myqnapcloud.com/index.html
- http://odiee.myqnapcloud.com/angular.html

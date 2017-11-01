### Polyfill RegExp to support named captures

Tested on IE 10+

#### Install
```
npm i regexp-polyfill --save
```

#### Documentation
[https://developers.google.com/web/updates/2017/07/upcoming-regexp-features](upcoming-regexp-features)

*WARN* The polyfill only works when creating RegExp with new. The syntax `/pattern/flags`won't work !

Currently only named captures are polyfilled.

#### Example:
```js
const pattern = new RegExp(?<year>\d{4})-(?<month>\d{2})-(?<day>\d{2}));
const result = pattern.exec('2017-07-10');
// result.groups.year === '2017'
// result.groups.month === '07'
// result.groups.day === '10'
```

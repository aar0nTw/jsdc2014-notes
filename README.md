Opening
==============
### Jeff Pope
#### Sencha.io, Managing Director of Asia Pacific Region

promote, promote, promote

---

R0 #1 Use Node Modules In The Browser With Browserify
==============
### maxwell ogden

[JS for Cats](http://jsforcats.com)

_requrie anywhere use Browserify_
in browser you can handle dom, node can use TCP/UDP
but everything else you can do two place both

*browserify handbook* on github [browserify-handbook](https://github.com/substack/browserify-handbook)

[*browserify-adventure*](github.com/substack/browserify-adventure)
Learning browserify

[*nodeschool*](nodeschool.io)
Learning node online

`npm install learnyounode`

A npm module that can help you learn nodejs

step by step using cli

* github nodeschool/taiwan
* browserify-transform
* [substack/brfs](https://github.com/substack/brfs)

[_packify_](https://github.com/maxogden/packify)
Pack all stylesheets and js file in one html file
images become base64 encode

npm install --save

`--save` will put it in your dependencies

[_morkdown_](https://github.com/rvagg/morkdown)

[_leveljs_](https://github.com/rvagg/leveljs)
LevelDB with js

voxel.js
blockplot

[requirebin](http://requirebin.com/)

[wzrd.in](http://wzrd.in/)

[http://stack.gl/](http://stack.gl/)

[_thealphanerd/sudoku_](https://github.com/thealphanerd/sudoku)
applciation sample of use browserify

[_beefy_](http://didact.us/beefy/)
tiny browserify server

[_watchify_](https://github.com/substack/watchify)
Watch and recompile while every time you change file

[_tape_](https://www.npmjs.org/package/tape)
a test framework

[testling](https://ci.testling.com/)

---

R0 #2 Private NPM for Company
=====================
### 蘇千
#### @fengmk2

[npm structure](http://blog.nodejs.org/2013/11/26/npm-post-mortem/)

### Why CNPM

* Easy Maintain / 容易維護
* Lower Cost / 很低成本
* Stable / 穩定可用
* Faster / 更快
* Simple / 簡單
* Open Source / 開源

Use `npm install cnpm` and assign private npm registry path

(Taobao mirror)[http://npm.taobao.org/]

### Why Private NPM

* Need fast and stable NPM service
* Publish private modules
* Control the modules of NPM

_What's the problem on CouchDB solution_

* Sync Latency too large

_CNPM_
- Duplicate name between public and private module.
- Internal User Authorization

Solve:
  - Scoped package, use namespace to avoid duplicate package name.
    Publish with @scoped
    e.g.: `@ali/fs`, `@alipay/fs`

  - CNPM support UserService API [http://t.cn/Rhr8Zes](http://t.cn/Rhr8Zes)
    - auth
    - get
    - list
    - search


Ali NPM Downloads per month in 2014 is grow to 2 millions.
(Paypal private npm have 500,000 npm installs per day, internally. 8x than Ali)

_Lower Cost_

[cnpmjs.org](http://cnpmjs.org) total cost per month: $19.6, only NT$ 600

_Stable_

[reports: r.cnpmjs.org](http://r.cnpmjs.org)

_Easy to contribute_

cnpm/cnpmjs

_koa_
[koajs/koa](https://github.com/koajs/koa)

They are hiring

- Javascript Engineer
- NodeJS Engineer
@ Alipay

suqian.yf@alipay.com

---

R0 #3 HTML Accessibility
============================
### 楊曉明
#### @lepture

### Accessibility Matters

[View Slide](http://lab.lepture.com/jsdc-2014/slide.html#/)

It is the right thing to do, Just follow the standards.

_Accessibility in real life_

  * The Metro
  * Toliet Design
  * Traffic Light, it's a bad design for color blindners.
    ~8% is color blinders in reallife
    Think about why we not add a shape for the light that make the color blinder can access the traffic light.

  Trello color blind friendly label.

[yue.css](http://lab.lepture.com/yue.css/)

> yue.css is a typography stylesheet for readable content.
> It was created for my blog at first since I always designed a new theme for my blog.
> But later it becomes the offical stylesheet for yuehu site.

[ChromeVox](http://www.chromevox.com/)

> ChromeVox is a screen reader for Chrome which brings the speed, versatility, and security of Chrome to visually impaired users.

[Accessibility Developer Tools](https://chrome.google.com/webstore/detail/accessibility-developer-t/fpkknkljclfencbdbgkenhalefipecmb)

> This extension will add an Accessibility audit, and an Accessibility sidebar pane in the Elements tab, to your Chrome Developer Tools.

[Spectrum](https://chrome.google.com/webstore/detail/spectrum/ofclemegkcmilinpcimpjkfhjfgmhieb)

> Instantly test your web page with different types of color vision deficiency.

---

R2 #4 Functional JavaScript, Why or Why Not?
============================================
### Greg Weng
#### @GregWeng

[View Slide](http://bit.ly/jsdc2014-funjs)

[Mozilla blog](http://blog.mozilla.com.tw/)

Functional Programming would bring you:
   * Re-thinking
   * Patterns
   * Fun

[facebook/immutable-js](https://github.com/facebook/immutable-js)

_Monad_

[What is a monad - StackOverflow](http://stackoverflow.com/questions/44965/what-is-a-monad)

It's so complex when we search monad on initernet.

Monadic actions can be chained as function composition.

[PoC of Maybe in Javascript](https://github.com/snowmantw/warmfuzzything.js/blob/master/maybe.js)

[React](http://facebook.github.io/react/index.html)

[Flux](http://facebook.github.io/flux/docs/overview.html)

[Facebook flux TodoMVC example](https://github.com/facebook/flux/tree/master/examples/flux-todomvc)


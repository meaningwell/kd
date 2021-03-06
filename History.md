
1.1.2 / 2015-04-20
==================

  * Merge pull request #17 from tetsuo/bug/pr-15-missing-returns
    * buttons: add missing return statements

1.1.1 / 2015-04-17
==================

  * Merge pull request #16 from alex-ionochkin/spotlightview-size-fix
    * spotlightview: code formatting
    * spotlightview: size fix
  * Merge branch 'patch/shortcuts-ui' into 1.2.0
    * list: do not let itemview to freak out when there is no data available
  * Merge pull request #15 from tetsuo/1.2.0
    * dia/scene/update-scene: throttle indeed :hatched_chick:
    * npm: add lodash@3.6.0
    * npm: remove lodash.throttle
    * expose debug
    * use debug instead of KD.error :balloon:
    * core/object: bind console.error instead of KD.error onError :hatched_chick:
    * core/windowctrl: use debug instead of KD.log :rabbit:
    * core/utils: log :arrow_right: console.log
    * core/router: use debug instead of KD.log
    * core/kd: use debug instead of console[log|warn|error] :hamster:
    * core/view: use debug to log lazyElement found warning
    * core/view: remove unused deprecated fn
    * core/view: remove obsolete appendToDOMBody
    * use console.log instead of KD.log to explicitly dump messages :cat:
    * split: remove obsolete methods :cop:
    * components: use debug instead of log/warn :hear_no_evil:
    * npm: add debug

1.1.0 / 2015-03-31
==================

 This release brings in some breaking api changes.

 * `core/keyboard` module is factored out to [shortcuts](https://github.com/koding/shortcuts)
 * `kd.KeyboardListener` & `kd.KeyboardMap` classes are obsolete along with all key-bindings stuff.
 * winctrl: remove obsolete viewHasKeyCombos
 * winctrl: do not register/unregister Mousetrap bindings
 * winctrl: remove obsolete superizeCombos
 * winctrl: currentCombos is obsolete
 * winctrl: keyViewHistory is obsolete
 * styles: chmod -x
 * utils: chmod -x
 * do not export keyboard
 * rm core/keyboard
 * npm: rm mousetrap
 * SplitView: Don't try to resize if there is no panel.

1.0.13 / 2015-03-20
==================

 * Merge pull request #12 from alex-ionochkin/90763920-custom-scroll-command-key
 * npm: bump up version
 * customscroll: key binding for command+up/down

1.0.11 / 2015-03-12
==================

 * Merge pull request #9 from sinan/kd.js
 * CustomScroll: removed nested hidden overflow

1.0.10 / 2015-03-08
==================

 * Merge pull request #8 from tetsuo/bump-up-jspath
 * npm: bump up jspath

1.0.9 / 2015-03-04
==================

 * Merge pull request #6 from alex-ionochkin/82401098-custom-scroll-keyboard-handling
 * customview: fix for incorrect constant name
 * customscroll: document keydown event unbinding, refactoring
 * customscroll: char code constants
 * customscroll: keyboard handling
 * Merge pull request #7 from sinan/get-rid-of-kdfsprite-and-sourcemaps-on-dist
 * styles: get rid of kdfsprite() util
 * dist: css/js w/o sourcemaps

1.0.7 / 2015-02-27
==================

 * windowController: focusChange improved (https://github.com/tetsuo/kd/pull/5)

1.0.6 / 2015-02-27
==================

 * Close dialog on ESC (https://github.com/tetsuo/kd/pull/4)

1.0.3 / 2015-02-19
==================

 * add changelog
 * bump up htmlencode

1.0.2 / 2015-02-19
==================

* `playground` folder is gone. Typing `make example` starts a simple development server and recompiles files upon changes in `example` folder
* added touch support to `scrollview`
* to watch `lib` folder and build a standalone umd package into `dist` folder, you type `make development-dist`
* to compile each file individually into `build` folder upon changes, type `make development`

1.0.1 / 2015-02-9
==================

* browserified and re-listed on npm as `kd.js`
* umd build (`dist/kd.js`) exposes only `kd` to global scope now on
* we are exporting all classes and methods without the `KD` prefix

Example:

```coffeescript
kd = require 'kd'

class X extends kd.View
```

* styl entry file is now being transpiled with `--include-css`
* `test` & `docs` became obsolete and removed
* `KD.EventEmitter.Wildcard` is changed to `kd.EventEmitterWildcard`
* `underscore` is removed
* `jquery-timeago` is changed with `timeago` package on npm
* added `kd.singleton` (alias for `kd.getSingleton`)
* moved `lib/themes` to `styles`
* all `window` calls/assignment are changed to `global` (see: browserify)
* removed `gulpfile`, added `Makefile`

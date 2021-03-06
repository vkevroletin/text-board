# TEXT BOARD [![Build Status](https://travis-ci.org/vkevroletin/text-board.png?branch=master)](https://travis-ci.org/vkevroletin/text-board) [![Coverage Status](https://coveralls.io/repos/vkevroletin/text-board/badge.png?branch=master)](https://coveralls.io/r/vkevroletin/text-board?branch=master)

Toy anonymous text board with live updates. If you're brave enough 
then you can check [unmoderated live example](http://vkevroletin.github.io/text-board/).
If someone made post which hurts you please contact me. I will reset database or will add button which
deletes posts from board.

Installation is simple
---

This is client-side javascript application. Power of quick live updates comes from [firebase](https://www.firebase.com/) service.

You need node.js installed in your system. Also you need bower and grunt-cli(if you plan to develop):

        npm install -g bower
        npm install -g grunt-cli

Clone source code using git and install bower dependencies:

        git clone https://github.com/vkevroletin/text-board.git
        cd text-board
        bower install

Development
---

Install npm dependencies which will automate your life.
They find errors in code, run tests in multiple browsers, optimize code and install libraries. 

        npm install

Workflow
---

Verify syntax in all javascript files
       
        grunt jshint

Run unit tests and write code coverage statistics into `coverage/` folder

        grunt test

Run unit tests each time you change code

        grunt watch:jsTest

Prepare distribution with optimized code into `dist` folder

        grunt build

Serve application using nodejs server (with autoreload feature)

        grunt serve

e2e testing
---

You need to install WebDriver and configure tests/protractor.conf.js. Then you are ready
to run tests.

Run e2e tests in chrome

        grunt test:e2e

Run e2e in other browser

        grunt protractor:firefox
        grunt protractor:chrome
        grunt protractor:opera
        grunt protractor:ie

Run e2e tests each time you change code:

        webdriver-manager start
        grunt watch:e2e


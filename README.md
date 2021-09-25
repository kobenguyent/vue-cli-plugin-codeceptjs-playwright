# vue-cli-plugin-e2e-codeceptjs-playwright

*Hey, how about some end 2 end testing for your Vue apps?* 🤔

*Let's do it together! Vue, [CodeceptJS](https://codecept.io) & [Playwright](https://playwright.dev) and myself.* 🤗

*Browser testing would be more fun. Just see it!* 😍

```js
I.amOnPage('/');
I.click('My Component Button');
I.see('My Component');
I.say('I am happy!');
// that's right, this is a valid test! 
```

## How to try it?

**Requirements:** 

* NodeJS >= 8.9.1
* NPM / Yarn
* Vue CLI installed globally

Note:

* CodeceptJS requires Node.js version 8.9.1+ or later.
* To use the parallel test execution, requiring Node.js version 11.7 or later.

```
npm i vue-cli-plugin-codeceptjs-playwright --save-dev
```

This will install CodeceptJS, CodeceptUI & Playwright.

To add CodeceptJS to your project, invoke the installer:

```
vue invoke vue-cli-plugin-codeceptjs-playwright
```

> You will be asked about installing a demo component. If you start a fresh project **it is recommended to agree and install a demo component**, so you could see tests passing.


## Running Tests

We added npm scripts:

* `test:e2e` - will execute tests with an opened browser . If you installed test component, and started a test server, running this command will show you a browser window passed test.
  * Use `--headless` option to run browser with headless mode
  * Use `--serve` option to start a dev server before tests 


Examples:

```
npm run test:e2e 
npm run test:e2e -- --headless
npm run test:e2e -- --serve 
```

> This command is a wrapper for `codecept run --steps`. You can use the [Run arguments and options](https://codecept.io/commands#run) here.

* `test:e2e:parallel` - will execute tests headlessly in parallel processes (workers). By default, runs tests in 2 workers.
  * Use an argument to set number of workers
  * Use `--serve` option to start dev server before running

Examples:

```
npm run test:e2e:parallel
npm run test:e2e:parallel -- 3
npm run test:e2e:parallel -- 3 --serve
```

> This command is a wrapper for `codecept run-workers 2`. You can use the [Run arguments and options](https://codecept.io/commands#run-workers) here.

* `test:e2e:open` - this opens interactive web test runner. So you could see, review & run your tests from a browser.

![](http://g.recordit.co/2oFa0LM0q6.gif)

```
npm run test:e2e:open
```

## Directory Structure

Generator has created these files:

```js
codecept.conf.js          👈 codeceptjs config
jsconfig.json             👈 enabling type definitons
tests
├── e2e
│   ├── app_test.js       👈 demo test, edit it!
│   ├── output            👈 temp directory for screenshots, reports, etc
│   └── support
│       └── steps_file.js 👈 common steps
└── steps.d.ts            👈 type definitions
```

If you agreed to create a demo component, you will also see `TestMe` component in `src/components` folder.

## How to write tests?

* Open `tests/e2e/app_js` and see the demo test
* Execute a test & use an interactive pause to see how CodeceptJS works
* [Learn CodeceptJS basics](https://codecept.io/basics)
* [Learn how to write CodeceptJS tests with Puppeteer](https://codecept.io/puppeteer)
* [See full reference for CodeceptJS Puppeteer Helper](https://codecept.io/helpers/Puppeteer)
* Ask your questions in [Slack](http://bit.ly/chat-codeceptjs) & [Forum](https://codecept.discourse.group/)

## Enjoy testing!

Testing is simple & fun, enjoy it! 

With ❤ [CodeceptJS Team](https://codecept.io)
# vue-cli-plugin-codeceptjs-playwright

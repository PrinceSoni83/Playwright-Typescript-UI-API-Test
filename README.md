[![Playwright Tests](https://github.com/PrinceSoni83/Playwright-Typescript-UI-API-Test/actions/workflows/playwright.yml/badge.svg)](https://github.com/PrinceSoni83/Playwright-Typescript-UI-API-Test/actions/workflows/playwright.yml)

# Playwright-Typescript-Page-Objects-API

Playwright demo scripts to automate ui flows using page object design pattern and typescript. The Repo also contains the automated api tests.

## About Framework

This framework is using the **Page Object Model** which is built using **Playwright** with **Typescript** and **Jest**. [Playwright](https://github.com/microsoft/playwright) is a single API for automating Chromium, Firefox, and WebKit. The [page object](https://playwright.dev/docs/pom) design pattern is used to capture the HTML elements.

## Installation

To start the project on our local machine, we must first clone this repository. Then, inside the repo, run `npm install` to download all of the project's dependencies. `npm init playwright@latest` will install the various browser configurations along with Playwright.

## Configuration

Playwright Test allows you to customise the default browser, context, and page fixtures. There are options such as `headless`, `viewport`, and `ignoreHTTPSErrors`. You can also capture a `screenshot` at the end of the test or record a `video` or a `trace` for it. There are numerous testing options, such as timeout and testDir, that allow you to customise how your tests are collected and executed. Any option can be specified globally in the configuration file and most of them locally in a test file.
See the full list of [test options](https://playwright.dev/docs/api/class-testoptions) and all [configuration properties](https://playwright.dev/docs/api/class-testconfig).
The reposigtory is configured to run three different projects : Web, API and Mobile (Playwrigh Device Emulation).

## Running Tests

We have the option to perform one test, a group of tests, or all tests. One browser or a number of browsers can be used to run tests. By default, tests are performed headlessly, which means no browser tabs are opened while they are being run and results are displayed in the terminal.

Run the following commands to execute differnt test suites, all the suits are configured to run in parallel.

- `npx playwright test --grep @web --project=web`
- `npx playwright test --grep @api --project=api`
- `npx playwright test --grep @web --project=mobile`

here is the list of [command line test run options](https://playwright.dev/docs/running-tests#command-line)

When a test fails, you can have it automatically run again by using test retries. This is helpful when a test is erratic and fails from time to time. The [configuration file](https://playwright.dev/docs/test-configuration) specifies the test retries.

## Debugging

`npx playwright test --debug`

Since Playwright runs in Node.js, thus we can debug it using your preferred debugger, such as 'console.log', your IDE, or the [VS Code Extension](https://playwright.dev/docs/getting-started-vscode). Playwright comes with the [Playwright Inspector](https://playwright.dev/docs/debug#playwright-inspector) that is included with Playwright enables you to step through Playwright API calls, view their debug logs, and investigate [selectors](https://playwright.dev/docs/api/class-selectors).

[UI Mode](https://playwright.dev/docs/test-ui-mode) lets you explore, run and debug tests with a time travel experience complete with watch mode.To open UI mode, run the following command in your terminal:

`npx playwright test --ui`

## Test Execution Report

A few built-in reporters for various needs are included with Playwright Test, and it also has the option to create custom reporters. Passing the `--reporter` command line option is the simplest approach to test out built-in reporters. Allure At the conclusion of the test execution, an HTML report with a failure **screenshot** and scenario will be generated. For the failed test scenarios, a trace **video** will be attached.

here are the steps to generate the allure report in local machine:

- Generate Allure Report: `allure generate ./allure-results -o ./allure-report --clean`
- Open Allure Report: `allure open ./allure-report`

Test Report Screenshots:
![alt text](image.png)
![alt text](image-1.png)
![alt text](image-2.png)

To learn more about test-reporters click [here](https://playwright.dev/docs/test-reporters)

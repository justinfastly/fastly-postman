# Fastly API Collection for Postman

This repository contains a [Postman](https://www.getpostman.com/) collection and an environment for the [Fastly API](https://docs.fastly.com/api/). The goal is to make the interaction with the API as easy as possible without running and modifying cURL commands every time from scratch. You just need to update the global and environment variables to get started. Once setup is complete, you have another handy option to control your [Fastly](https://www.fastly.com/) account and services!

![Banner](/screenshots/banner.png?raw=true "Fastly API Collection for Postman")

## Table of Contents

- [Prerequisites](#prerequisites)
- [Install](#install)
- [API Coverage](#api-coverage)
- [Usage](#usage)
- [Tests](#tests)
- [Contribute](#contribute)

## Prerequisites

You'll need [Postman](https://www.getpostman.com/) in order to get started. Postman is a far better replacement of [cURL](https://curl.haxx.se/)! You can either add the [Postman Extension](https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop?hl=en-US) to your [Chrome](https://www.google.com/chrome/browser/desktop/index.html?brand=CHBD&gclid=CIHNlY--r9ICFUaNfgodSrEJFg) web browser or you can download the free [Postman App](https://www.getpostman.com/).

## Install

Clone or download this repository and open [Postman](https://www.getpostman.com/). I recommend to clone it by typing the following command in your terminal:

```
$ git clone https://github.com/philippschulte/fastlyApiCollection.git
```

This way it is easier to fetch the latest changes by typing:

```
$ git pull origin master
```

Fastly is constantly updating their API and I'll try to keep up with them. By pulling the latest changes from the master branch you can avoid downloading the repository over and over again!

Then you need to import the collection, environment, and globals `JSON` file. Click on the [Import](#usage) button on the top bar, and drag and drop:

```
fastly.postman_collection.json
fastly.postman_environment.json
fastly.postman_globals.json
```

You'll maybe notice an error message like:

```
Failed to import data: Could not import: TypeError: Cannot read property 'id' of null
```

Important is that you see the following messages:

- Collection Fastly imported
- Environment Fastly imported
- Globals imported

**Don't worry about the error message! I don't know why Postman is throwing this error but I have tested the setup and everything is working like a charm!**

## API Coverage

The following libraries are not part of this collection yet:

- [Remote logging](https://docs.fastly.com/api/logging)
- [Utilities](https://docs.fastly.com/api/tools)
- [Web Application Firewall](https://docs.fastly.com/api/waf)
- [Dynamic Servers](https://docs.fastly.com/api/dynamicservers)

Some API endpoints require session authentication. These endpoints are not included even if Postman’s native apps provide a Cookie Manager. Below is a list of all supported libraries of the [Fastly API](https://docs.fastly.com/api/):

| Category         | Collection Requests | API Requests | Coverage |
| :--------------- | :------------------ | :----------- | :------- |
| ACL              | 5                   | 5            | 100%     |
| ACL Entry        | 6                   | 6            | 100%     |
| API Tokens       | 6                   | 6            | 100%     |
| Backend          | 5                   | 5            | 100%     |
| Billing          | 1                   | 1            | 100%     |
| Billing Address  | 2                   | 4            | 50%      |
| Cache Settings   | 5                   | 5            | 100%     |
| Condition        | 5                   | 5            | 100%     |
| Customer         | 5                   | 5            | 100%     |
| Dictionary       | 5                   | 5            | 100%     |
| Dictionary Item  | 7                   | 7            | 100%     |
| Diff             | 1                   | 1            | 100%     |
| Director         | 5                   | 5            | 100%     |
| Director Backend | 3                   | 3            | 100%     |
| Domain           | 7                   | 7            | 100%     |
| Event Logs       | 2                   | 2            | 100%     |
| Gzip             | 5                   | 5            | 100%     |
| Header           | 5                   | 5            | 100%     |
| Healthcheck      | 5                   | 5            | 100%     |
| Historical Stats | 8                   | 8            | 100%     |
| Invitation       | 3                   | 3            | 100%     |
| Pricing Extras   | 2                   | 2            | 100%     |
| Purging          | 4                   | 4            | 100%     |
| Request Settings | 5                   | 5            | 100%     |
| Response Object  | 5                   | 5            | 100%     |
| Service          | 8                   | 8            | 100%     |
| Settings         | 2                   | 2            | 100%     |
| Soft Purging     | 2                   | 2            | 100%     |
| Stats            | 1                   | 1            | 100%     |
| User             | 7                   | 7            | 100%     |
| VCL              | 11                  | 11           | 100%     |
| VCL Snippets     | 7                   | 7            | 100%     |
| Version          | 9                   | 9            | 100%     |
|                  | **159**             | **161**      | **99%**  |

## Usage

1. Click on the `Manage Environments` button and select the `Fastly` environment. Update all key/value pairs with your account credentials and service information. The `password` and `username` properties are only necessary to be able to create new API tokens.

![Update Environment Variables](/screenshots/usage_1.png?raw=true "Update Environment Variables")

2. Click on the `Manage Environments` button and select the `Fastly` environment. Rename the environment to your first service name and hit the `Update` button. Then click the `Duplicate Environment` button to clone the environment for each of your services. Select each environment to update the name to your service name and update the values for `service_id`, `service_name`, and `version_no`.

![Duplicate Environments](/screenshots/usage_2.png?raw=true "Duplicate Environments")

3. Take a look at the screenshot below to get familiar with the basic Postman functionality. The Postman application has a very intuitive UI but in case you are looking for more information please look at their [docs](https://www.getpostman.com/docs/). **Don't forget to select the proper service environment from the drop-down list before you fire any requests!**

![Basic Postman Functionality](/screenshots/usage_3.png?raw=true "Basic Postman Functionality")

4. Another great feature of [Postman](https://www.getpostman.com/) is that you can generate code snippets for cURL and most server side languages. All you need to do is to click on the `Generate Code Snippets` link and select your favorite language. Keep in mind that you are able to modify and copy the snippet.

![Generate Code Snippets](/screenshots/usage_4.png?raw=true "Generate Code Snippets")

5. That's not everything! [Postman](https://www.getpostman.com/) also generates a beautiful documentation of the entire collection. Toggle the `Details Toolbar` and click the `View Docs` button to open the documentation in your web browser.

![Open Documentation](/screenshots/usage_5.png?raw=true "Open Documentation")

6. The collection provides the description, headers, body, and a sample request for all endpoints. **Each request description provides a link to the Fastly docs to redirect you to the associated endpoint documentation!** You can switch the environment and choose your prefered language to generate a sample request with the associated variables. You can copy the request to the clipboard and paste it into your scripts.

![Documentation](/screenshots/usage_6.png?raw=true "Documentation")

**Keep in mind that you can always extend the collection and environment functionality by adding more requests and variables. You can customize it for your needs. Don't forget to hit the `Save` button whenever you make changes you want to persist. Fastly is constantly updating their API. Please [contribute](#contribute) if you find any requests which are not covered, incomplete, or outdated.**

## Tests

The main feature of [Postman](https://www.getpostman.com/) is testing APIs. With Postman you can write and run tests for each request using the JavaScript language. Postman allows you to loop through the data returned by an API and perform sequential requests and tests using that data. It contains a powerful runtime based on [Node.js](https://nodejs.org/en/) that allows you to add dynamic behavior to requests and collections. This allows you to write test suites, build requests that can contain dynamic parameters, pass data between requests, and a lot more. You can add JavaScript code to execute during 2 events in the flow:

1. Before a request is sent to the server, as a [pre-request script](https://www.getpostman.com/docs/postman/scripts/pre_request_scripts) under the Pre-request Script tab.
2. After a response is received, as a [test script](https://www.getpostman.com/docs/postman/scripts/test_scripts) under the Tests tab.

Whatever code you write in these sections is executed in the [Postman Sandbox](https://www.getpostman.com/docs/postman/scripts/postman_sandbox). To check what is available in the sandbox, take a look at the [documentation](https://www.getpostman.com/docs/postman/scripts/postman_sandbox). Postman tries to make the process easier by listing commonly used snippets next to the editor. You can select the snippet you want to add and the appropriate code will be added to the test editor. This is a great way to quickly build test cases.

Results are displayed in a `Tests` tab under the response viewer. The tab header shows how many tests passed, and the keys that you set in the tests variable are listed here. If the value evaluates to true, the test passed.

![Postman Sandbox](/screenshots/usage_7.png?raw=true "Postman Sandbox")

The [Postman Collection Runner](https://www.getpostman.com/docs/postman/collection_runs/starting_a_collection_run) allows you to run either the entire collection or a single library against a corresponding environment. **Don't forget to select an environment before you run your tests!**

![Postman Collection Runner](/screenshots/usage_8.png?raw=true "Postman Collection Runner")

I know that a lot of Fastly users build their own scripts to automate requests to the Fastly API. [Postman’s Newman Tool](https://www.getpostman.com/docs/postman/collection_runs/command_line_integration_with_newman) allows you to run and test a Postman Collection directly from the command line. It is built with extensibility in mind so that you can easily integrate it with your continuous integration servers and build systems.

![Postman’s Newman Tool](/screenshots/usage_9.png?raw=true "Postman’s Newman Tool")

**I have added to each request at least one assertion to test the status code. I wanted to keep the collection as simple as possible. Feel free to add as many assertions to the collection as you like and as necessary for your needs!**

## Contribute

In general, I follow the "fork-and-pull" Git workflow.

 1. **Fork** the repo on GitHub
 2. **Clone** the project to your own machine
 3. **Commit** changes to your own branch
 4. **Push** your work back up to your fork
 5. Submit a **Pull request** so that I can review your changes

NOTE: Be sure to merge the latest from "upstream" before making a pull request!

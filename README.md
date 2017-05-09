# Fastly API Collection for Postman

This repository contains a [Postman](https://www.getpostman.com/) collection and an environment for the [Fastly API](https://docs.fastly.com/api/). The goal is to make the interaction with the API as easy as possible without running and modifying curl commands every time from scratch. You just have to update the environment variables with your account credentials to get started. Once setup is complete, you have another handy option to control your [Fastly](https://www.fastly.com/) account and services!

![Banner](/screenshots/banner.png?raw=true "Fastly API Collection for Postman")

## Table of Contents

- [Prerequisites](#prerequisites)
- [Install](#install)
- [API Coverage](#api-coverage)
- [Usage](#usage)
- [Contribute](#contribute)

## Prerequisites

You'll need [Postman](https://www.getpostman.com/) in order to get started. Postman is a far better replacement of [cURL](https://curl.haxx.se/)! You can either add the [Postman Extension](https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop?hl=en-US) to your [Chrome](https://www.google.com/chrome/browser/desktop/index.html?brand=CHBD&gclid=CIHNlY--r9ICFUaNfgodSrEJFg) web browser or you can download the free [Postman App](https://www.getpostman.com/).

## Install

Clone or download this repository and open [Postman](https://www.getpostman.com/). You need to import the collection and environment `json` file. The repository provides the Postman collection format `v2`. The `v2` format is compared to `v1` more versatile and the most-used choice! Please read [this](http://blog.getpostman.com/2015/06/05/travelogue-of-postman-collection-format-v2/) article if you want to learn more about the different collection formats.

Click on the [Import](#usage) button on the top bar, and drag and drop:

```
fastly_postman_collection.json
fastly_postman_environment.json
```

**You can delete the `fastlyApiCollection` folder after you have imported the collection and environment!**

## API Coverage

At the moment the collection contains **0** out of **166** (not including Real-time analytics and Remote logging) requests. **More requests are coming soon!** Some API endpoints require session authentication. These endpoints are not included even if Postman’s native apps provide a Cookie Manager. Below is a list of all supported libraries of the [Fastly API](https://docs.fastly.com/api/):

> Fastly announced that account-level API keys will be retired in favor of personal API tokens on May 15th, 2017. This collection and environment is only supporting API tokens! It's a piece of cake to create an API token with Postman if you don't have one yet!

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
| Customer         | 2                   | 5            | 40%      |
| Dictionary       | 5                   | 5            | 100%     |
| Dictionary Item  | 7                   | 7            | 100%     |
| Diff             | 1                   | 1            | 100%     |
| Director         | 5                   | 5            | 100%     |
| Director Backend | 3                   | 3            | 100%     |
| Domain           | 7                   | 7            | 100%     |
| Event Log        | 1                   | 1            | 100%     |
| Event Logs       | 2                   | 2            | 100%     |
| Gzip             | 5                   | 5            | 100%     |
| Header           | 5                   | 5            | 100%     |
| Healthcheck      | 5                   | 5            | 100%     |
| Request Settings | 5                   | 5            | 100%     |
| Response Object  | 5                   | 5            | 100%     |
| Service          | 8                   | 8            | 100%     |
| Settings         | 2                   | 2            | 100%     |
| Stats            | 1                   | 1            | 100%     |
| VCL              | 11                  | 11           | 100%     |
| Version          | 9                   | 9            | 100%     |
| Wordpress        | 5                   | 5            | 100%     |
|                  | **129**             | **134**      | **96%**  |

## Usage

1. Click on the `Manage Environments` button and select the `Fastly` environment. Update all key/value pairs with your account credentials and service information.

![Update Environment Variables](/screenshots/usage_1.png?raw=true "Update Environment Variables")

2. Click on the `Manage Environments` button and select the `Fastly` environment. Rename the environment to your first service name and hit the `Update` button. Then click the `Duplicate Environment` button to clone the environment for each of your services. Select each environment to update the name to your service and update the values for `service_id` and `service_name`.

![Duplicate Environments](/screenshots/usage_2.png?raw=true "Duplicate Environments")

3. Take a look at the screenshot below to get familiar with the basic Postman functionality. The Postman application has a very intuitive UI but in case you are looking for more information please look at their [docs](https://www.getpostman.com/docs/). **Don't forget to make sure you have selected the proper service environment before you fire any requests!**

![Basic Postman Functionality](/screenshots/usage_3.png?raw=true "Basic Postman Functionality")

4. Another great feature of [Postman](https://www.getpostman.com/) is that you can generate code snippets for most command line and server side languages. All you need to do is to click on the `Generate Code Snippets` link and select your favorite language. Keep in mind that you are able to modify and copy the snippet.

![Generate Code Snippets](/screenshots/usage_4.png?raw=true "Generate Code Snippets")

5. That's not everything! [Postman](https://www.getpostman.com/) also generates generates a beautiful documentation of the entire collection. Toggle the `Details Toolbar` and click the `View Docs` button to open the documentation in your web browser.

![Open Documentation](/screenshots/usage_5.png?raw=true "Open Documentation")

6. The documentation provides the description, headers, body, and a sample request for all endpoints. You can switch the environment and choose your prefered language to generate a sample request with the associated variables. You can copy the request to the clipboard and paste it into your scripts to fire requests to the [Fastly API](https://docs.fastly.com/api/) outside of [Postman](https://www.getpostman.com/).

![Documentation](/screenshots/usage_6.png?raw=true "Documentation")

Keep in mind that you can always extend the collection and environment functionality buy adding more endpoints and variables. Don't forget to hit the `Save` button whenever you make changes you want to persist. Fastly is constantly updating the API. Please [contribute](#contribute) if you find any requests which are not covered, incomplete, or outdated.

## Contribute

In general, I follow the "fork-and-pull" Git workflow.

 1. **Fork** the repo on GitHub
 2. **Clone** the project to your own machine
 3. **Commit** changes to your own branch
 4. **Push** your work back up to your fork
 5. Submit a **Pull request** so that I can review your changes

NOTE: Be sure to merge the latest from "upstream" before making a pull request!

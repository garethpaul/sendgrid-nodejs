[![BuildStatus](https://travis-ci.org/sendgrid/sendgrid-nodejs.svg?branch=master)](https://travis-ci.org/sendgrid/sendgrid-nodejs)
[![npm version](https://badge.fury.io/js/%40sendgrid%2Fclient.svg)](https://badge.fury.io/js/%40sendgrid%2Fclient)
[![Email Notifications Badge](https://dx.sendgrid.com/badge/nodejs)](https://dx.sendgrid.com/newsletter/nodejs)

**This package is part of a monorepo, please see [this README](https://github.com/sendgrid/sendgrid-nodejs/blob/master/README.md) for details.**

# Mail Service for the Sendgrid v3 Web API
This is a dedicated service for interaction with the mail endpoint of the [Sendgrid v3 API](https://sendgrid.com/docs/API_Reference/api_v3.html).

To be notified when this package is updated, please subscribe to email [notifications](https://dx.sendgrid.com/newsletter/nodejs) for releases and breaking changes.

# Installation

## Prerequisites

- Node.js version 6, 7 or 8
- The SendGrid service, starting at the [free level](https://sendgrid.com/free?source=sendgrid-nodejs)

## Setup Environment Variables

Update the development environment with your [SENDGRID_API_KEY](https://app.sendgrid.com/settings/api_keys), for example:

```bash
echo "export SENDGRID_API_KEY='YOUR_API_KEY'" > sendgrid.env
echo "sendgrid.env" >> .gitignore
source ./sendgrid.env
```

## Install Package

The following recommended installation requires [npm](https://npmjs.org/). If you are unfamiliar with npm, see the [npm docs](https://npmjs.org/doc/). Npm comes installed with Node.js since node version 0.8.x therefore you likely already have it.

```sh
npm install --save @sendgrid/mail
```

You may also use [yarn](https://yarnpkg.com/en/) to install.

```sh
yarn add @sendgrid/mail
```

<a name="quick_start"></a>
# Quick Start, Hello Email

For more complex use cases, please see [USE_CASES.md](https://github.com/sendgrid/sendgrid-nodejs/blob/master/packages/mail/USE_CASES.md).

```js
const sgMail = require('@sendgrid/mail');
sgMail.setApiKey(process.env.SENDGRID_API_KEY);
const msg = {
  to: 'test@example.com',
  from: 'test@example.com',
  subject: 'Sending with SendGrid is Fun',
  text: 'and easy to do anywhere, even with Node.js',
  html: '<strong>and easy to do anywhere, even with Node.js</strong>',
};
sgMail.send(msg);
```

<a name="troubleshooting"></a>
# Troubleshooting

Please see our [troubleshooting guide](https://github.com/sendgrid/sendgrid-nodejs/blob/master/TROUBLESHOOTING.md) for common library issues.

<a name="announcements"></a>
# Announcements

All updates to this library are documented in our [CHANGELOG](https://github.com/sendgrid/sendgrid-nodejs/blob/master/CHANGELOG.md) and [releases](https://github.com/sendgrid/sendgrid-nodejs/releases). You may also subscribe to email [release notifications](https://dx.sendgrid.com/newsletter/nodejs) for releases and breaking changes.

<a name="roadmap"></a>
# Roadmap

If you are interested in the future direction of this project, please take a look at our open [issues](https://github.com/sendgrid/sendgrid-nodejs/issues) and [pull requests](https://github.com/sendgrid/sendgrid-nodejs/pulls). We would love to hear your feedback.

<a name="contribute"></a>
# How to Contribute

We encourage contribution to our libraries (you might even score some nifty swag), please see our [CONTRIBUTING](https://github.com/sendgrid/sendgrid-nodejs/blob/master/CONTRIBUTING.md) guide for details.

* [Feature Request](https://github.com/sendgrid/sendgrid-nodejs/tree/master/CONTRIBUTING.md#feature_request)
* [Bug Reports](https://github.com/sendgrid/sendgrid-nodejs/tree/master/CONTRIBUTING.md#submit_a_bug_report)
* [Improvements to the Codebase](https://github.com/sendgrid/sendgrid-nodejs/tree/master/CONTRIBUTING.md#improvements_to_the_codebase)

<a name="troubleshooting"></a>
# Troubleshooting

Please see our [troubleshooting guide](https://github.com/sendgrid/sendgrid-nodejs/blob/master/TROUBLESHOOTING.md) for common library issues.

<a name="about"></a>
# About

@sendgrid/mail is guided and supported by the SendGrid [Developer Experience Team](mailto:dx@sendgrid.com).

@sendgrid/mail is maintained and funded by SendGrid, Inc. The names and logos for @sendgrid/mail are trademarks of SendGrid, Inc.

![SendGrid Logo](https://uiux.s3.amazonaws.com/2016-logos/email-logo%402x.png)
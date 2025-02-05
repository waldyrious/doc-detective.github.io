---
title: Get started
layout: default
nav_order: 2
---

# Get started

Doc Detective is versatile, and you can deploy it in many ways to suit the requirements of your development environment. This guide covers the most common deployment methods: NPM and CLI.

## NPM

Doc Detective integrates with Node projects as an NPM package. When using the NPM package, you must specify all options in the `test()` method's `config` argument, which is a JSON object with the same structure as [config.json](https://github.com/doc-detective/doc-detective/blob/main/sample/config.json).

1.  In a terminal, navigate to your Node project and install Doc
    Detective:
    ```bash
    npm install doc-detective
    ```
2.  In your project, add a reference to the package:
    ```javascript
    const { test } = require("doc-detective");
    ```
3.  Run tests with the `test(config)` method:
    ```javascript
    test(config);
    ```

## CLI

You can run Doc Detective as a standalone CLI tool. When running as a CLI tool, you can specify default configuration options in [config.json](https://github.com/doc-detective/doc-detective/blob/main/sample/config.json) and override those defaults with command-line arguments. (For a list of arguments, complete the following steps and run `npm run test -- -h`.)

1. Install prerequisites:
   - Node.js
2. In a terminal, clone the repo and install dependencies:

   ```bash
   git clone https://github.com/doc-detective/doc-detective.git
   cd doc-detective
   npm install
   ```

2. Run tests according to your config. The -c argument is required and specifics the path to your config. The following example runs tests in the [sample/](https://github.com/doc-detective/doc-detective/tree/main/sample) directory:

   ```bash
   npm run test -- -c sample/config.json
   ```

To customize your test, file type, and directory options, update [sample/config.json](https://github.com/doc-detective/doc-detective/blob/main/sample/config.json)

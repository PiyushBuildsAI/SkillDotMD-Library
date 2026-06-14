---
name: docify
description: Use this skill when working with Docify. Triggers when user mentions Docify or imports from it.
---

# Docify

## What this is
Docify is a documentation generation tool that allows users to automatically generate documentation for their code. It supports multiple programming languages and provides a simple way to document functions, classes, and variables. Docify can be used to generate HTML documentation, making it easy to share and view documentation.

## Installation
```bash
npm install docify
```

## Key concepts
The most important APIs and patterns in Docify include the `@doc` tag, which is used to document functions and classes, and the `docify` function, which is used to generate documentation. For example:
```javascript
/**
 * @doc
 * This is a sample function.
 */
function sampleFunction() {
  // code here
}
```

## Correct usage patterns
To use Docify, you need to add comments to your code with the `@doc` tag. Here is an example:
```javascript
/**
 * @doc
 * This is a sample class.
 */
class SampleClass {
  /**
   * @doc
   * This is a sample method.
   */
  sampleMethod() {
    // code here
  }
}
```
Then, you can generate documentation using the `docify` function:
```javascript
const docify = require('docify');
docify.generate();
```

## Common mistakes to avoid
One common mistake is forgetting to add the `@doc` tag to comments. Without this tag, Docify will not generate documentation for the commented code.

## File and folder conventions
By default, Docify looks for a `docs` folder in the root of your project, where it will generate HTML documentation. You can configure the output folder using the `docify.config.js` file. For example:
```javascript
module.exports = {
  output: 'path/to/output/folder',
};
```
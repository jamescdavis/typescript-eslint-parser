# TypeScript ESLint Parser

A parser that converts TypeScript source code into an [ESTree](https://github.com/estree/estree)-compatible form.

**Important:** This parser is not fully compatible with all ESLint rules and plugins. Some rules will improperly mark source code as failing or not find problems where it should.

## Supported TypeScript Version

We will always endeavor to support the latest stable version of TypeScript.

The version of TypeScript currently supported by this parser is `~2.8.1`. This is reflected in the `devDependency` requirement within the package.json file, and it is what the tests will be run against. We have an open `peerDependency` requirement in order to allow for experimentation on newer/beta versions of TypeScript.

If you use a non-supported version of TypeScript, the parser will log a warning to the console.

**Please ensure that you are using a supported version before submitting any issues/bug reports.**

## Known Issues

The following ESLint rules will fail on acceptable code:
 - no-undef [#416](https://github.com/eslint/typescript-eslint-parser/issues/416)
 
The follow ESLint plugins have issues when used with this parser:
 - eslint-plugin-import
    - prefer-default-export - Will fail exports inside of Namespaces or Modules

## Usage

Install:

```
npm i typescript-eslint-parser --save-dev
```

And in your ESLint configuration file:

```
"parser": "typescript-eslint-parser"
```

## Help Wanted!

If you're familiar with TypeScript and ESLint, and you'd like to see this project progress, please consider contributing. We need people with a good knowledge of TypeScript to ensure this parser is useful.

## Reporting Bugs

Please check the current list of open and known issues and ensure the bug has not been reported before. When creating a new issue provide as much information about your environment as possible. This includes:
 - ESLint Version
 - TypeScript version
 - TypeScript parser version
 - ESLint config or rules and plugins currently enabled

As well include a small code sample that can be used to reproduce the issue.

## Contributing

Issues and pull requests will be triaged and responded to as quickly as possible. We operate under the [ESLint Contributor Guidelines](http://eslint.org/docs/developer-guide/contributing), so please be sure to read them before contributing. If you're not sure where to dig in, check out the [issues](https://github.com/eslint/typescript-eslint-parser/issues).

## Build Commands

* `npm test` - run all linting and tests
* `npm run lint` - run all linting
* `npm run ast-alignment-tests` - run only Babylon AST alignment tests
* `npm run integration-tests` - run only integration tests

## License

TypeScript ESLint Parser is licensed under a permissive BSD 2-clause license.

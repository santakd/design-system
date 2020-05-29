# Salesforce Lightning Design System

[![Build Status](https://travis-ci.org/salesforce-ux/design-system.svg?branch=master)](https://travis-ci.org/salesforce-ux/design-system)

Welcome to the source code repository for [Salesforce Lightning Design System](http://getslds.com/), brought to you by [Salesforce UX](https://twitter.com/salesforceux).

SLDS is...

* Tailored for building Salesforce apps: Using the Lightning Design System markup and CSS framework results in UIs that reflect the Salesforce Lightning look and feel.
* Continuously updated: As long as you’re using the latest version of the Lightning Design System, your pages are always up to date with Salesforce UI changes.

## Getting Started

This project utilizes Storybook for component development. If you would like to know more about Storybook or how it works, check out [their website](https://storybook.js.org/).

### **Project Installation & Setup:**

1. Clone the repository down locally.
2. `cd` into the project and run `npm install` to install all project dependencies.

### Running the Development Environment:

If you've just installed the project, you will need to run `npm run full-start` to first perform a full build, which is necessary for Storybook to operate.

Whenever you add or remove a component, you'll want to perform this full-start. Otherwise, you can just run `npm start` to start the Storybook server without a build.

## Developing in Storybook

Once the development server is started with `npm start`, you can load it at [http://localhost:9002](http://localhost:9002/).

### Annotations

See the [annotations guide](https://github.com/salesforce-ux/design-system-internal/blob/226-summer-20/guidelines/ANNOTATIONS.md).

## Tasks

### `npm start`

Starts the Storybook server for local development.

### `npm run full-start`

Performs a full build and dist before starting the Storybook server. Useful for when a component or utility is added or removed from the system.

### `npm run gulp -- lint`

Lint the code base for syntax and stylistic errors.

```
# Lint indentation, Sass, JavaScript files
npm run gulp -- lint

# Lint languages independently
npm run gulp -- lint:sass
npm run gulp -- lint:javascript
npm run gulp -- lint:javascript:test
npm run gulp -- lint:spaces
npm run gulp -- lint:html

# HTML5 validation
npm run gulp -- lint:vnu
# HTML5 validation on comma separated blueprint names
npm run gulp -- lint:vnu --components button,path,trees

# a11y validation
npm run gulp -- lint:a11y
# a11y validation on comma separated blueprint names
npm run gulp -- lint:a11y --components button,path,trees

# Lint examples using vnu, aXe, slds validation, and HTML5 validation
npm run gulp -- lint:examples
```

### Pull Request Checks

To run all the checks a pull request will run in Travis use the following command.

```
# To run every check against all blueprints
npm run pr-checks

# To run every check but target certain blueprints for slow checks like aXe and vnu
npm run pr-checks -- --components button,path,trees
```

### Compilation

`npm run build-dist`

Generate the Lightning Design System into the `.dist` directory.

`npm run gulp -- styles`

Compile Sass to CSS into `.assets/styles`.

`npm run gulp -- clean`

Delete temporary build and local files.

### Stats

`npm run gulp -- styles:stats`: Useful stats about the project's deliverables.

### Tests

`npm test`: run all tests

## Troubleshooting

See the [troubleshooting guide](https://github.com/salesforce-ux/design-system-internal/blob/226-summer-20/guidelines/TROUBLESHOOTING.md).

## Contributing Back to SLDS

See the [contributing guide](https://github.com/salesforce-ux/design-system-internal/blob/226-summer-20/CONTRIBUTING.md).

## Licenses

* Source code is licensed under [BSD 3-Clause](https://git.io/sfdc-license)
* All icons and images are licensed under [Creative Commons Attribution-NoDerivatives 4.0](https://github.com/salesforce-ux/licenses/blob/master/LICENSE-icons-images.txt)
* The Salesforce Sans font is licensed under our [font license](https://github.com/salesforce-ux/licenses/blob/master/LICENSE-font.txt)

## Got Feedback?

Please open a new [GitHub Issue](https://github.com/salesforce-ux/design-system/issues).

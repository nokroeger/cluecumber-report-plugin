# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

Back to [Readme](README.md).

## [1.5.0] - 2018-11-08

### Added

* Full support for png, gif, png, jpg, svg, html, xml, json, text and pdf attachments (contributed by @Rameshwar244)
* Minor design improvements

## [1.4.2] - 2018-10-16

### Fixed

* Attachments work in step before/after hooks

### Added

* Option to hide/show step hooks on the "Scenario Details" page (only present if the scenario has step hooks in at least one step)

## [1.4.1] - 2018-10-09

### Added

* `skip` property for skipping the report generation completely.

### Fixed

* Corrected typo on `All Tags` page.

## [1.4.0] - 2018-09-06

### Changed

* Cleaner layout without unnecessary horizontal lines
* Tables now show 25 entries by default
* Changed internal package structure

### Added

* Scenario Sequence page that shows the order of scenario executions and their states without deviding them into separate `passed`, `failed` and `skipped` sections 
* Option to show/hide docstrings on the "Scenario Details" page (only present if the scenario has docstrings in at least one step)

### Fixed

* Long data tables broke the layout

## [1.3.0] - 2018-08-21

### Added

* `customCSS` property to provide an additional CSS file that is loaded on top of Cluecumber's default styles
* Support for step doc strings

### Changed

* Replaced `passed`, `failed` and `skipped` descriptions by webfont symbols
* Cleaned up information box content on all pages
* Data tables now use the full report width
* Stack traces are now formatted

## [1.2.1] - 2018-07-31

### Fixed

* Scenario calculation is now in line with the official Cucumber recommendations:
    * Scenarios with a mixture of passing and failing steps are now reported as passed
    * Scenarios with ONLY skipped steps and skipped or passing hooks will be reported as skipped
    * Scenarios with failing scenario or step hooks are reported as failed

## [1.2.0] - 2018-07-27

### Fixed

* Support for parameter highlighting in [Karate](https://github.com/intuit/karate/) tests
* Hiding skipped steps from the scenario detail chart now also hides steps that are _considered_ skipped but have a status other than `skipped`

### Added

* Failed Cucumber 3 `BeforeStep` and `AfterStep` hooks are shown on failure
* SVG attachment support

### Changed

* Separated `Before` and `After` hooks from steps in detail view
* Cleaned up "All Features" and "All Tags" charts
* Aligned and streamlined design on all pages

## [1.1.1] - 2018-07-03

### Fixed

* Page rendering error on certain step name characters

## [1.1.0] - 2018-07-03

### Added

* Synchronize charts and displayed data for "All Scenarios" and "Scenario Details" pages
* Improved highlighting of steps on mouseover

### Changed

* Charts now show more relevant information

### Fixed

* Parameter highlighting with regex characters does not crash report generation
* Correct chart labels for steps

## [1.0.0] - 2018-06-21

### Added

* New page "All Features"
* New page "All Tags"
* New page "Scenarios by Tag"
* New page "Scenarios by Feature"
* Parameters in steps are now highlighted

## [0.8.0] - 2018-06-10

### Fixed

* Scenario.write outputs with null values lead to rendering exceptions
* Scenario.write outputs are not shown in before and after steps

### Added

* Support for Before and After hock attachments
* Updated example JSON files in example project

### Removed

* Capitalization of scenario names

## [0.7.1] - 2018-05-08

### Added

* Feature description is now shown in the feature tool tip on hover

### Fixed

* Chart was not rendered when a scenario contained step data tables

## [0.7.0] - 2018-04-18

### Changed

* Unified report design
* Updated all dependencies
* Completely changed freemarker code to be better extensible

## [0.6.0] - 2018-04-12

### Added

* Example project

### Changed

* Cluecumber is now a monorepo

### Fixed

* Table header error on tab overview page

## [0.5.0] - 2018-03-19

### Added

* Tag summary page

### Fixed

* Background Scenario steps are now rendered correctly
* Various small bug fixes

## [0.3.0] - 2018-02-19

### Added

* Scenario.output is now displayed in the scenario details

### Fixed

* Scenarios with pending and skipped steps are also considered skipped.
* Background scenarios are now merged to the following scenarios.

### Changed

* Before and after steps have a lower opacity to focus on test steps.
* Internal organization of page types allows easier extension.

## [0.2.0] - 2018-01-16

### Added

- Support for data tables within steps
- Cleaner report headers

### Removed

- Javascript back method is replaced with simple links on the detail pages

### Fixed

- Report generation is now much more resilient if information is missing in the JSON sources

## [0.1.1] - 2017-12-12

### Removed

- Unnecessary log outputs for attachments

## [0.1.0] - 2017-12-12

### Added

- Support for Cucumber 2 attachments

## [0.0.6] - 2017-11-29

### Fixed

- missing hook durations could crash during report generation
- back link fix for iframed report

### Added

- More unit tests

## [0.0.5] - 2017-11-20

### Fixed

- Tooltips are rendered correctly on data table page switch
- html encoding in stacktraces fixed
- back link also supports iframes

### Added

- Custom properties can be added to the report, URL will automatically be clickable
- Before and After hooks are displayed in the report
- Total test time is shown in the start page
- Tool tips for feature file names
- Tool tips for scenario step method signatures

## [0.0.4] - 2017-11-20

### Added

- Scenario duration is displayed on start page
- Feature file name is displayed on feature name mouse over

### Fixed

- Corrupt or empty JSON files do not fail report generation anymore

## [0.0.3] - 2017-11-15

### Fixed

- handling of scenarios without steps
- handling of undefined steps

## [0.0.2] - 2017-11-14

Initial project version on GitHub and Maven Central.

[1.5.0]: https://github.com/trivago/cluecumber-report-plugin/tree/1.5.0
[1.4.2]: https://github.com/trivago/cluecumber-report-plugin/tree/1.4.2
[1.4.1]: https://github.com/trivago/cluecumber-report-plugin/tree/1.4.1
[1.4.0]: https://github.com/trivago/cluecumber-report-plugin/tree/1.4.0
[1.3.0]: https://github.com/trivago/cluecumber-report-plugin/tree/1.3.0
[1.2.1]: https://github.com/trivago/cluecumber-report-plugin/tree/1.2.1
[1.2.0]: https://github.com/trivago/cluecumber-report-plugin/tree/1.2.0
[1.1.1]: https://github.com/trivago/cluecumber-report-plugin/tree/1.1.1
[1.1.0]: https://github.com/trivago/cluecumber-report-plugin/tree/1.1.0
[1.0.0]: https://github.com/trivago/cluecumber-report-plugin/tree/1.0.0
[0.8.0]: https://github.com/trivago/cluecumber-report-plugin/tree/0.8.0
[0.7.1]: https://github.com/trivago/cluecumber-report-plugin/tree/0.7.1
[0.6.0]: https://github.com/trivago/cluecumber-report-plugin/tree/0.6.0
[0.5.0]: https://github.com/trivago/cluecumber-report-plugin/tree/0.5.0
[0.3.0]: https://github.com/trivago/cluecumber-report-plugin/tree/0.3.0
[0.2.0]: https://github.com/trivago/cluecumber-report-plugin/tree/0.2.0
[0.1.1]: https://github.com/trivago/cluecumber-report-plugin/tree/0.1.1
[0.1.0]: https://github.com/trivago/cluecumber-report-plugin/tree/0.1.0
[0.7.0]: https://github.com/trivago/cluecumber-report-plugin/tree/0.0.7
[0.0.6]: https://github.com/trivago/cluecumber-report-plugin/tree/0.0.6
[0.0.5]: https://github.com/trivago/cluecumber-report-plugin/tree/0.0.5
[0.0.4]: https://github.com/trivago/cluecumber-report-plugin/tree/0.0.4
[0.0.3]: https://github.com/trivago/cluecumber-report-plugin/tree/0.0.3
[0.0.2]: https://github.com/trivago/cluecumber-report-plugin/tree/0.0.2
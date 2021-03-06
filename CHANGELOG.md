# CHANGELOG

2.0.0/ 2016.09.22
=================

### Breaking changes
#### Namespace

The `Statsd` is now namespaced under the Datadog module.

To update:
- `require 'statsd'` -> `require 'datadog/statsd`
- `Statsd` -> `Datadog::Statsd`

#### Tags

`,` is now stripped from tags to avoid unexpected behavior.

`Datadog::Statsd` also validates that it receives an array of tags, and strips `,` and `|` from them.

1.6.0/ 2015.12.21
==================

### Changes

* [IMPROVEMENT] Stop mutating input parameters, [#22][] [@olefriis][]

1.5.0/ 2015.05.20
==================

### Notice

This release drops testing for Ruby 1.8.7.
Future versions are likely to introduce backward incompatibilities with < Ruby 1.9.3.

### Changes

* [FEATURE] Add service checks support, [#11][]
* [FEATURE] Send time stat on failing block, [#16][] [@gleseur][]
* [BUGFIX] Add instance tags to `Statsd.event`, [#14][] [@gleseur][]
* [OTHER] Use `send_stat` instead of overriding Ruby `send` method, [#17][] [@sensadrome][]
* [OTHER] Changelog update

1.4.1/ 2014.09.29
==================

### Changes

* [BUGFIX] Fixed bug in message separator when batching metrics

1.4.0/ 2014.06.13
==================

### Changes

* [FEATURE] Added support for metrics batching

1.3.0/ 2014.03.27
==================

### Changes

* [FEATURE] Added support for submitting events

1.2.0/ 2013.07.10
==================

### Changes

* [FEATURE] Added global tags
* [FEATURE] Added ability to set namespace and tags from `Statsd#initialize`

1.1.0/ 2012.09.21
==================

### Changes

* [FEATURE] Added sets metrics

1.0.0/ 2012.06.14
==================

### Changes

* Initial release


<!--- The following link definition list is generated by PimpMyChangelog --->
[#11]: https://github.com/DataDog/dogstatsd-ruby/issues/11
[#14]: https://github.com/DataDog/dogstatsd-ruby/issues/14
[#16]: https://github.com/DataDog/dogstatsd-ruby/issues/16
[#17]: https://github.com/DataDog/dogstatsd-ruby/issues/17
[#22]: https://github.com/DataDog/dogstatsd-ruby/issues/22
[@gleseur]: https://github.com/gleseur
[@olefriis]: https://github.com/olefriis
[@sensadrome]: https://github.com/sensadrome

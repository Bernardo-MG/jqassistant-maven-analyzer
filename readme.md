# JQAssistant Maven Analyzer

Maven project for analyzing with JQAssistant.

Can be used by itself, as a gateway to use JQAssistant. Or may be used as a basis to set up JQAssistant on a Maven project.

[![Release docs](https://img.shields.io/badge/docs-release-blue.svg)][site-release]
[![Development docs](https://img.shields.io/badge/docs-develop-blue.svg)][site-develop]

[![Release javadocs](https://img.shields.io/badge/javadocs-release-blue.svg)][javadoc-release]
[![Development javadocs](https://img.shields.io/badge/javadocs-develop-blue.svg)][javadoc-develop]

## Features

- Ready to use JQAssistant setup

## Documentation

Documentation is always generated for the latest release, kept in the 'master' branch:

- The [latest release documentation page][site-release].
- The [latest release Javadoc site][javadoc-release].

Documentation is also generated from the latest snapshot, taken from the 'develop' branch:

- The [the latest snapshot documentation page][site-develop].
- The [latest snapshot Javadoc site][javadoc-develop].

### Building the docs

The documentation site is actually a Maven site, and its sources are included in the project. If required it can be generated by using the following Maven command:

```
$ mvn verify site
```

The verify phase is required, otherwise some of the reports won't be generated.

## Usage

The project makes use of the [JQAssistant plugin][jqassistant-plugin]. To analyze just run the integration verify phase:

```
$ mvn clean verify -Dscan.path=[path to project]
```

Using the clean goal is recommended. On big projects it is faster than waiting for the database to be repopulated.

Afterwards just start the server:

```
mvn jqassistant:server
```

This will give access to two dashboards, one for Neo4J, another for JQAssistant:

| URL                                         | Dashboard     |
| ------------------------------------------- | ------------- |
| http://localhost:7474                       | Neo4j         |
| http://localhost:7474/jqassistant/dashboard | JQAssistant   |

## Collaborate

Any kind of help with the project will be well received, and there are two main ways to give such help:

- Reporting errors and asking for extensions through the issues management
- or forking the repository and extending the project

### Issues management

Issues are managed at the GitHub [project issues tracker][issues], where any Github user may report bugs or ask for new features.

### Getting the code

If you wish to fork or modify the code, visit the [GitHub project page][scm], where the latest versions are always kept. Check the 'master' branch for the latest release, and the 'develop' for the current, and stable, development version.

## License

The project has been released under the [MIT License][license].

[bintray-repo]: https://bintray.com/bernardo-mg/maven/jqassistant-maven-analyzer/view
[maven-repo]: http://mvnrepository.com/artifact/com.bernardomg.jqassistant/jqassistant-maven-analyzer
[issues]: https://github.com/bernardo-mg/jqassistant-maven-analyzer/issues
[javadoc-develop]: https:///jqassistant-maven-analyzer/apidocs
[javadoc-release]: https:///jqassistant-maven-analyzer/apidocs
[license]: https://www.opensource.org/licenses/mit-license.php
[scm]: https://github.com/bernardo-mg/jqassistant-maven-analyzer
[site-develop]: https:///jqassistant-maven-analyzer
[site-release]: https:///jqassistant-maven-analyzer

[jqassistant-plugin]: https://github.com/kontext-e/jqassistant-plugins

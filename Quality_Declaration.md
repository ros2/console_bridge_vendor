
This document is a declaration of software quality for the `console_bridge_vendor` package, based on the guidelines in [REP-2004](https://www.ros.org/reps/rep-2004.html).

# `console_bridge_vendor` Quality Declaration

The package `console_bridge_vendor` claims to be in the **Quality Level 1** category.

Below are the rationales, notes, and caveats for this claim, organized by each requirement listed in the [Package Requirements for Quality Level 1 in REP-2004](https://www.ros.org/reps/rep-2004.html).

## Version Policy

### Version Scheme

`console_bridge_vendor` uses `semver` according to the recommendation for ROS Core packages in the [ROS 2 Developer Guide](https://index.ros.org/doc/ros2/Contributing/Developer-Guide/#versioning), and is at or above a stable version, i.e. `>= 1.0.0`.

### API Stability Within a Released ROS Distribution

TODO: Define policy to handle ABI stability for vendor packages

### ABI Stability Within a Released ROS Distribution

TODO: Define policy to handle ABI stability for vendor packages

### Public API Declaration

TODO: Define API for this package

## Change Control Process

`console_bridge_vendor` follows the recommended guidelines for ROS Core packages in the [ROS 2 Developer Guide](https://index.ros.org/doc/ros2/Contributing/Developer-Guide/#change-control-process).

This includes:

- all changes occur through a pull request
- all pull request have two peer reviews
- all pull request must pass CI on all [tier 1 platforms](https://www.ros.org/reps/rep-2000.html#support-tiers)
- all pull request must resolve related documentation changes before merging

## Documentation

### Feature Documentation

TODO fix link. Current state: There is some documentation on its latest [wiki](http://wiki.ros.org/console_bridge).

`console_bridge_vendor` has a [feature list](TODO) and each item in the list links to the corresponding feature documentation.
There is documentation for all of the features, and new features require documentation before being added.

### Public API Documentation

TODO fix link

`console_bridge_vendor` has embedded API documentation and it is generated using doxygen and is [hosted](TODO) along side the feature documentation.
There is documentation for all of the public API, and new additions to the public API require documentation before being added.

### License

The license for `console_bridge_vendor` is Apache 2.0, and a summary is in each source file, the type is declared in the `package.xml` manifest file, and a full copy of the license is in the `LICENSE` file.

There is an automated test which runs a linter (ament_copyright) that ensures each file has a license statement.

### Copyright Statements

The copyright holders each provide a statement of copyright in each source code file in `console_bridge_vendor`.

There is an automated test which runs a linter (ament_copyright) that ensures each file has at least one copyright statement.

## Testing

### Feature Testing

Each feature in `console_bridge_vendor` has corresponding tests which simulate typical usage, and they are located in the in the tests for the [test](https://github.com/ros/console_bridge/tree/master/test) folder of the `libconsole-bridge-dev` library.

New features are required in the external library require to be tested before being added to this package.

### Public API Testing
TODO: Define API for this package

Each part of the public API have tests, and new additions or changes to the public API require tests before being added.
The tests aim to cover both typical usage and corner cases, but are quantified by contributing to code coverage.

### Coverage

TODO fix link, how to handle coverage for external dependencies?

`console_bridge_vendor` follows the recommendations for ROS Core packages in the [ROS 2 Developer Guide](https://index.ros.org/doc/ros2/Contributing/Developer-Guide/#coverage), and opts to use branch coverage instead of line coverage.

This includes:

- tracking and reporting branch coverage statistics
- achieving and maintaining branch coverage at or above 95%
- no lines are manually skipped in coverage calculations

Changes are required to make a best effort to keep or increase coverage before being accepted, but decreases are allowed if properly justified and accepted by reviewers.

### Performance

`console_bridge_vendor` follows the recommendations for performance testing of vendor packages in the [ROS 2 Developer Guide](https://index.ros.org/doc/ros2/Contributing/Developer-Guide/#performance), and opts to do performance analysis on each release rather than each change.

TODO Will this package require performance testing?

### Linters and Static Analysis

`console_bridge_vendor` uses and passes all the standard linters and static analysis tools for a vendored package as described in the [ROS 2 Developer Guide](https://index.ros.org/doc/ros2/Contributing/Developer-Guide/#linters-and-static-analysis). This includes using ament_lint_common to analyze the package manifest and its cmake files for correct syntax.

TODO any qualifications on what "passing" means for certain linters

## Dependencies

TODO: Quality declaration document for the external dependency

`console_bridge_vendor` depends directly on the external dependency `libconsole-bridge-dev`, this one was qualified as quality level 1 as described thoroughly [QD libconsole-bridge-dev](TODO).

## Platform Support

`console_bridge_vendor` supports all of the tier 1 platforms as described in [REP-2000](https://www.ros.org/reps/rep-2000.html#support-tiers), and tests each change against all of them.

TODO make additional statements about non-tier 1 platforms?
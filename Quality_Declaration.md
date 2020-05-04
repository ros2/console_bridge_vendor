This document is a declaration of software quality for the `console_bridge_vendor` package, based on the guidelines in [REP-2004](https://www.ros.org/reps/rep-2004.html).

# `console_bridge_vendor` Quality Declaration

The package `console_bridge_vendor` claims to be in the **Quality Level 4** category.

Below are the rationales, notes, and caveats for this claim, organized by each requirement listed in the [Package Quality Categories in REP-2004](https://index.ros.org/doc/ros2/Contributing/Developer-Guide/#package-quality-categories) of the ROS2 developer guide.

## Version Policy [1]

### Version Scheme [1.i]

`console_bridge_vendor` uses `semver` according to the recommendation for ROS Core packages in the [ROS 2 Developer Guide](https://index.ros.org/doc/ros2/Contributing/Developer-Guide/#versioning).

### Version Stability [1.ii]

`console_bridge_vendor` is at or above a stable version, i.e. `>= 1.0.0`.

### Public API Declaration [1.iii]

External dependency is loaded downloaded from upstream and there is no public API declaration hosted for `libconsole-bridge-dev`.

### API Stability Policy [1.iv]

`console_bridge_vendor` is pinned to a `libconsole-bridge-dev` version (Currently 0.4.1), so it will not break public API within a released ROS distribution, i.e. no major releases once the ROS distribution is released.

### ABI Stability Policy [1.v]

`console_bridge_vendor` is pinned to a `libconsole-bridge-dev` version (Currently 0.4.1), so it will not break public ABI within a released ROS distribution, i.e. no major releases once the ROS distribution is released.

### ABI and ABI Stability Within a Released ROS Distribution [1.vi]

`console_bridge_vendor` will not break API nor ABI within a released ROS distribution, i.e. no major releases once the ROS distribution is released.

## Change Control Process [2]

`console_bridge_vendor` follows the recommended guidelines for ROS Core packages in the [ROS 2 Developer Guide](https://index.ros.org/doc/ros2/Contributing/Developer-Guide/#change-control-process).

### Change Requests [2.i]

All changes will occur through a pull request, check [ROS 2 Developer Guide](https://index.ros.org/doc/ros2/Contributing/Developer-Guide/#change-control-process) for additional information.

### Contributor Origin [2.ii]

This package uses DCO as its confirmation of contributor origin policy. More information can be found in [CONTRIBUTING](../CONTRIBUTING.md).

### Peer Review Policy [2.iii]

All pull requests will be peer-reviewed, check [ROS 2 Developer Guide](https://index.ros.org/doc/ros2/Contributing/Developer-Guide/#change-control-process) for additional information.

### Continuous Integration [2.iv]

This package is not being tested under ROS2 CI.

###  Documentation Policy [2.v]

All pull requests must resolve related documentation changes before merging.

## Documentation [3]

### Feature Documentation [3.i]

There is some documentation on its latest [wiki](http://wiki.ros.org/console_bridge). This information might require to be updated and expanded further for the use of `console_bridge_vendor`.

### Public API Documentation [3.ii]

`console_bridge_vendor` does not have Public API Documentation.

### License [3.iii]

The license for `console_bridge_vendor` is Apache 2.0, and a summary is in each source file, the type is declared in the [`package.xml`](./package.xml) manifest file, and a full copy of the license is in the `LICENSE` file.

### Copyright Statements [3.iv]

The copyright holders each provide a statement of copyright in each source code file in `console_bridge_vendor`.

## Testing [4]

### Feature Testing [4.i]

`console_bridge_vendor` does not have features testing.

### Public API Testing [4.ii]

`console_bridge_vendor` does not have Public API testing.

### Coverage [4.iii]

`console_bridge_vendor` does not provide coverage testing.

### Performance [4.iv]

`console_bridge_vendor` does not provide performance testing.

### Linters and Static Analysis [4.v]

`console_bridge_vendor` is not being tested with linters or static analysis tools.

## Dependencies [5]

### Direct and Optional Runtime ROS Dependencies [5.i]/[5.ii]

`console_bridge_vendor` does not have direct/optional runtime ROS dependencies.

### Direct Runtime non-ROS Dependency [5.iii]

`console_bridge_vendor` depends directly on the external dependency `libconsole-bridge-dev`, this one is qualified as quality level 4 as described thoroughly [QD libconsole-bridge-dev](./libconsole-drige-dev_QD.md).

## Platform Support [6]

`console_bridge_vendor` supports all of the tier 1 platforms as described in [REP-2000](https://www.ros.org/reps/rep-2000.html#support-tiers).

## Security [7]

### Vulnerability Disclosure Policy [7.i]

This package does not yet have a Vulnerability Disclosure Policy.

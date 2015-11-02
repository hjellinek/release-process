

## Repos
- server
- compliance
- schemas
- (future) Java client
- (future) Python client
- build   [home of `repo` tool configuration]

## Three types of branches
- master
- release
- topic

## All HEADs must pass Continuous Integration (CI)

## Lifecycle Rules
- CI: all masters always build and pass tests
- Release: Release tags/branches always consistent across all repos
- Develop: Automatic creation of topic branches across all repos
- Topic CI: A PR against a topic branch must pass CI to be merged

## Version numbers
The ref server and other components are free to use their own version numbering
scheme, but cross-repo releases must be tagged with cross-repo version
numbers.

For example: the same Ref Server can have a Ref Server-local tag
calling it e.g. version `0.2.1abedfc`, but it and its corresponding
`schemas` commit would also be tagged as e.g. `ga4gh_release_0.6.0`.

![Release process flow](releases.png)

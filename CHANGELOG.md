# Changelog

All notable changes to this project are documented in this file.

## [Unreleased]

### Breaking changes

- **No longer generates `Debug`.** `#[derive(PageFrame)]` now implements only
  the traits needed by `PageFrame`, its `PhysAddr` supertrait and their users:
  `Clone`, `Copy`, `PartialEq`, `Eq`, `PartialOrd`, `Ord`, `Add` and `Sub`.
  Add `Debug` to the derive list explicitly if you need to format the address
  type: `#[derive(PageFrame, Debug)]`.

# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [8.2.0]
### Added
- Adds `signAuthorization` method for EIP-7702 ([#407](https://github.com/MetaMask/eth-sig-util/pull/407))

## [8.1.2]
### Changed
- Bump `@metamask/abi-utils` from `^2.0.4` to `^3.0.0` ([#405](https://github.com/MetaMask/eth-sig-util/pull/405))
- Bump `@metamask/utils` from `^9.0.0` to `^11.0.1` ([#405](https://github.com/MetaMask/eth-sig-util/pull/405))

## [8.1.1]
### Fixed
- Revert "fix: Add Permit type schema" ([#401](https://github.com/MetaMask/eth-sig-util/pull/401))

## [8.1.0]
### Added
- Add `Permit` type to `signTypedData` schema ([#399](https://github.com/MetaMask/eth-sig-util/pull/399))

## [8.0.0]
### Changed
- **BREAKING**: Values of type `number` are not accepted as address parameter anymore. Valid values are `string` and `Uint8Array`. ([#391](https://github.com/MetaMask/eth-sig-util/pull/391))
- **BREAKING**: Drop support for Node.js versions 16, 21. ([#390](https://github.com/MetaMask/eth-sig-util/pull/390))

## [7.0.3]
### Changed
- Bump `@metamask/abi-utils` to `^2.0.4` ([#381](https://github.com/MetaMask/eth-sig-util/pull/381))
- Bump `@metamask/utils` from `^9.0.0` ([#381](https://github.com/MetaMask/eth-sig-util/pull/381))

## [7.0.2]
### Fixed
- Replace dependency `tweetnacl-util` with `@scure/base` ([#358](https://github.com/MetaMask/eth-sig-util/pull/358))

## [7.0.1]
### Changed
- Remove dependency `ethjs-util` ([#349](https://github.com/MetaMask/eth-sig-util/pull/349))

### Fixed
- **BREAKING**: fix: interpret 0x as hex in bytes encodeField ([#354](https://github.com/MetaMask/eth-sig-util/pull/354))
  - This fixes a regression introduced in `6.0.1` which caused inconsistent signatures when data was supplied as literal `0x`.
- fix: Exclude test files from published release ([#350](https://github.com/MetaMask/eth-sig-util/pull/350))
- fix: Bump @babel/traverse from 7.21.5 to 7.23.2 ([#341](https://github.com/MetaMask/eth-sig-util/pull/341))

## [7.0.0]
### Changed
- **BREAKING**: Increase minimum Node.js version to v16 ([#332](https://github.com/MetaMask/eth-sig-util/pull/332))
- **BREAKING**: Bump `@metamask/abi-utils` from `^1.0.2` to `^2.0.2` ([#326](https://github.com/MetaMask/eth-sig-util/pull/336))
- Bump `@metamask/utils` from `^5.0.2` to `^8.1.0` ([#333](https://github.com/MetaMask/eth-sig-util/pull/333))

## [6.0.1]
### Changed
- Swap out legacy `ethereumjs-abi` for `@metamask/abi-utils` ([#319](https://github.com/MetaMask/eth-sig-util/pull/319))

### Fixed
- Bump `ethereum-cryptography` from `^2.0.0` to `^2.1.2` ([#302](https://github.com/MetaMask/eth-sig-util/pull/302))
- Bump `ethereumjs/util` from `^8.0.6` to `^8.1.0` ([#302](https://github.com/MetaMask/eth-sig-util/pull/302))
- Remove unused dependency `bn.js` (#334)  ([#302](https://github.com/MetaMask/eth-sig-util/pull/302))

## [6.0.0]
### Changed
- **BREAKING**: Fix `normalize` for empty strings and `0` ([#315](https://github.com/MetaMask/eth-sig-util/pull/315))
  - This is breaking as it changes the behavior of the function with an empty string or `0` as input: it will now return `0x` for an empty string and `0x00` for `0`, instead of `undefined`

## [5.1.0]
### Changed
- rawEncode: fix broken BigNumber negativity check ([#307](https://github.com/MetaMask/eth-sig-util/pull/307))
- Specify type interface for multiple functions ([#307](https://github.com/MetaMask/eth-sig-util/pull/307))
- Improve `type` parameter input validation ([#307](https://github.com/MetaMask/eth-sig-util/pull/307))
- deps: bn.js@4.11.8->4.12.0 ([#309](https://github.com/MetaMask/eth-sig-util/pull/309))
- devDeps: Support TypeScript version ~4.8.4 ([#307](https://github.com/MetaMask/eth-sig-util/pull/307))

## [5.0.3]
### Changed
- Bump ethereum-cryptography, @ethereumjs/util ([#302](https://github.com/MetaMask/eth-sig-util/pull/302))

## [5.0.2]
### Changed
- allow `bn.js` to resolve any minor/patch version above 4.11.8 ([#280](https://github.com/MetaMask/eth-sig-util/pull/280))

## [5.0.1]
### Fixed
- Fix issue introduced in `v5.0.0` where the method `encodeField` encoded fields typed as `bytes` and passed as hexstrings were encoded differently than previous versions ([#271](https://github.com/MetaMask/eth-sig-util/pull/271), [#274](https://github.com/MetaMask/eth-sig-util/pull/274))

## [5.0.0] [DEPRECATED]
### Changed
- **BREAKING:** Removed support for Node v12 in favor of v14 ([#137](https://github.com/MetaMask/eth-json-rpc-middleware/pull/137))
- Replace heavy crypto packages for lighter noble implementations via upgrading `ethereumjs-util` to latest (now called `@ethereumjs/util`) ([#260](https://github.com/MetaMask/eth-sig-util/pull/260))
- Migrate to Yarn 3 ([#264](https://github.com/MetaMask/eth-sig-util/pull/264))


## [4.0.1]
### Fixed
- Fix mistake in TYPED_MESSAGE_SCHEMA ([#243](https://github.com/MetaMask/eth-sig-util/pull/243))
  - The schema changed in v4 in a way that accidentally disallowed "reference types" (i.e. custom types) apart from the primary type. Reference types are now once again allowed.

## [4.0.0]
### Added
- **BREAKING**: Add subpath exports ([#214](https://github.com/MetaMask/eth-sig-util/pull/214), [#211](https://github.com/MetaMask/eth-sig-util/pull/211))
  - This is breaking because it prevents the import of modules that are not exposed as subpath exports.
- Add `salt` to the EIP-712 `domain` type ([#176](https://github.com/MetaMask/eth-sig-util/pull/176))
- Add additional unit tests ([#146](https://github.com/MetaMask/eth-sig-util/pull/146), [#164](https://github.com/MetaMask/eth-sig-util/pull/164), [#167](https://github.com/MetaMask/eth-sig-util/pull/167), [#169](https://github.com/MetaMask/eth-sig-util/pull/169), [#172](https://github.com/MetaMask/eth-sig-util/pull/172), [#177](https://github.com/MetaMask/eth-sig-util/pull/177), [#180](https://github.com/MetaMask/eth-sig-util/pull/180), [#170](https://github.com/MetaMask/eth-sig-util/pull/170), [#171](https://github.com/MetaMask/eth-sig-util/pull/171), [#178](https://github.com/MetaMask/eth-sig-util/pull/178), [#173](https://github.com/MetaMask/eth-sig-util/pull/173), [#182](https://github.com/MetaMask/eth-sig-util/pull/182), [#184](https://github.com/MetaMask/eth-sig-util/pull/184), [#185](https://github.com/MetaMask/eth-sig-util/pull/185), [#187](https://github.com/MetaMask/eth-sig-util/pull/187))
- Improve documentation ([#157](https://github.com/MetaMask/eth-sig-util/pull/157), [#177](https://github.com/MetaMask/eth-sig-util/pull/177), [#174](https://github.com/MetaMask/eth-sig-util/pull/174), [#180](https://github.com/MetaMask/eth-sig-util/pull/180), [#178](https://github.com/MetaMask/eth-sig-util/pull/178), [#181](https://github.com/MetaMask/eth-sig-util/pull/181), [#186](https://github.com/MetaMask/eth-sig-util/pull/186), [#212](https://github.com/MetaMask/eth-sig-util/pull/212), [#207](https://github.com/MetaMask/eth-sig-util/pull/207), [#213](https://github.com/MetaMask/eth-sig-util/pull/213))

### Changed
- **BREAKING**: Consolidate `signTypedData` and `recoverTypedSignature` functions ([#156](https://github.com/MetaMask/eth-sig-util/pull/156))
  - The functions `signTypedDataLegacy`, `signTypedData`, and `signTypedData_v4` have been replaced with a single `signTypedData` function with a `version` parameter. The `version` parameter determines which type of signature you get.
    - If you used `signTypedDataLegacy`, switch to `signTypedData` with the version `V1`.
    - If you used `signTypedData`, switch to `signTypedData` with the version `V3`.
    - If you used `signTypedData_v4`, switch to `signTypedData` with the version `V4`.
  - The functions `recoverTypedSignatureLegacy`, `recoverTypedSignature`, and `recoverTypedSignature_v4` have been replaced with a single `recoverTypedSignature` function.
    - If you used `recoverTypedSignatureLegacy`, switch to `recoverTypedMessage` with the version `V1`.
    - If you used `recoverTypedMessage`, switch to `recoverTypedMessage` with the version `V3`.
    - If you used `recoverTypedSignature_v4`, switch to `recoverTypedMessage` with the version `V4`.
- **BREAKING**: Rename `TypedDataUtils.sign` to `TypedDataUtils.eip712Hash` ([#104](https://github.com/MetaMask/eth-sig-util/pull/104))
  - This function never actually signed anything. It just created a hash that was later signed. The new name better reflects what the function does.
- **BREAKING**: Move package under `@metamask` npm organization ([#162](https://github.com/MetaMask/eth-sig-util/pull/162))
  - Update your `require` and `import` statements to import `@metamask/eth-sig-util` rather than `eth-sig-util`.
- **BREAKING**: Simplify function type signatures ([#198](https://github.com/MetaMask/eth-sig-util/pull/198))
  - This is only a breaking change for TypeScript projects that were importing types used by the function signatures. The types should be far simpler now.
  - The `TypedData` has been updated to be more restrictive (it only allows valid typed data now), and it was renamed to `TypedDataV1`
- **BREAKING**: Replace `MsgParams` parameters with "options" parameters ([#204](https://github.com/MetaMask/eth-sig-util/pull/204))
  - This affects the following functions:
    - `personalSign`
    - `recoverPersonalSignature`
    - `extractPublicKey`
    - `encrypt`
    - `encryptSafely`
    - `decrypt`
    - `decryptSafely`
    - `signTypedData`
    - `recoverTypedSignature`
  - All parameters are passed in as a single "options" object now, instead of the `MsgParams` type that was used for most of these functions previously. Read each function signature carefully to ensure you are correctly passing in parameters.
  - `personalSign` example:
    - Previously it was called like this: `personalSign(privateKey, { data })`
    - Now it is called like this: `personalSign({ privateKey, data })`
- **BREAKING**: Rename `Version` type to `SignTypedDataVersion` ([#218](https://github.com/MetaMask/eth-sig-util/pull/218))
- **BREAKING**: Rename `EIP712TypedData` type to `TypedDataV1Field` ([#218](https://github.com/MetaMask/eth-sig-util/pull/218))
- Add `signTypedData` version validation ([#201](https://github.com/MetaMask/eth-sig-util/pull/201))
- Add validation to check that parameters aren't nullish ([#205](https://github.com/MetaMask/eth-sig-util/pull/205))
- Enable inline sourcemaps ([#159](https://github.com/MetaMask/eth-sig-util/pull/159))
- Update `ethereumjs-util` to v6 ([#138](https://github.com/MetaMask/eth-sig-util/pull/138), [#195](https://github.com/MetaMask/eth-sig-util/pull/195))
- Allow `TypedDataUtils` functions to be called unbound ([#152](https://github.com/MetaMask/eth-sig-util/pull/152))
- Update minimum `tweetnacl-util` version ([#155](https://github.com/MetaMask/eth-sig-util/pull/155))
- Add Solidity types to JSON schema for `signTypedData` ([#189](https://github.com/MetaMask/eth-sig-util/pull/189))
- Replace README API docs with generated docs ([#213](https://github.com/MetaMask/eth-sig-util/pull/213))

## [3.0.1] - 2021-02-04
### Changed
- Update `ethereumjs-abi` ([#96](https://github.com/MetaMask/eth-sig-util/pull/96))
- Remove unused dependencies ([#117](https://github.com/MetaMask/eth-sig-util/pull/117))
- Update minimum `tweetnacl` to latest version ([#123](https://github.com/MetaMask/eth-sig-util/pull/123))

## [3.0.0] - 2020-11-09
### Changed
- [**BREAKING**] Migrate to TypeScript ([#74](https://github.com/MetaMask/eth-sig-util/pull/74))
- Fix package metadata ([#81](https://github.com/MetaMask/eth-sig-util/pull/81)
- Switch from Node.js v8 to Node.js v10 ([#76](https://github.com/MetaMask/eth-sig-util/pull/77) and [#80](https://github.com/MetaMask/eth-sig-util/pull/80))


## [2.5.4] - 2021-02-04
### Changed
- Update `ethereumjs-abi` ([#121](https://github.com/MetaMask/eth-sig-util/pull/121))
- Remove unused dependencies ([#120](https://github.com/MetaMask/eth-sig-util/pull/120))
- Update minimum `tweetnacl` to latest version ([#124](https://github.com/MetaMask/eth-sig-util/pull/124))

## [2.5.3] - 2020-03-16 [WITHDRAWN]
### Changed
- [**BREAKING**] Migrate to TypeScript ([#74](https://github.com/MetaMask/eth-sig-util/pull/74))
- Fix package metadata ([#81](https://github.com/MetaMask/eth-sig-util/pull/81)
- Switch from Node.js v8 to Node.js v10 ([#76](https://github.com/MetaMask/eth-sig-util/pull/77) and [#80](https://github.com/MetaMask/eth-sig-util/pull/80))

[Unreleased]: https://github.com/MetaMask/eth-sig-util/compare/v8.2.0...HEAD
[8.2.0]: https://github.com/MetaMask/eth-sig-util/compare/v8.1.2...v8.2.0
[8.1.2]: https://github.com/MetaMask/eth-sig-util/compare/v8.1.1...v8.1.2
[8.1.1]: https://github.com/MetaMask/eth-sig-util/compare/v8.1.0...v8.1.1
[8.1.0]: https://github.com/MetaMask/eth-sig-util/compare/v8.0.0...v8.1.0
[8.0.0]: https://github.com/MetaMask/eth-sig-util/compare/v7.0.3...v8.0.0
[7.0.3]: https://github.com/MetaMask/eth-sig-util/compare/v7.0.2...v7.0.3
[7.0.2]: https://github.com/MetaMask/eth-sig-util/compare/v7.0.1...v7.0.2
[7.0.1]: https://github.com/MetaMask/eth-sig-util/compare/v7.0.0...v7.0.1
[7.0.0]: https://github.com/MetaMask/eth-sig-util/compare/v6.0.1...v7.0.0
[6.0.1]: https://github.com/MetaMask/eth-sig-util/compare/v6.0.0...v6.0.1
[6.0.0]: https://github.com/MetaMask/eth-sig-util/compare/v5.1.0...v6.0.0
[5.1.0]: https://github.com/MetaMask/eth-sig-util/compare/v5.0.3...v5.1.0
[5.0.3]: https://github.com/MetaMask/eth-sig-util/compare/v5.0.2...v5.0.3
[5.0.2]: https://github.com/MetaMask/eth-sig-util/compare/v5.0.1...v5.0.2
[5.0.1]: https://github.com/MetaMask/eth-sig-util/compare/v5.0.0...v5.0.1
[5.0.0]: https://github.com/MetaMask/eth-sig-util/compare/v4.0.1...v5.0.0
[4.0.1]: https://github.com/MetaMask/eth-sig-util/compare/v4.0.0...v4.0.1
[4.0.0]: https://github.com/MetaMask/eth-sig-util/compare/v3.0.1...v4.0.0
[3.0.1]: https://github.com/MetaMask/eth-sig-util/compare/v3.0.0...v3.0.1
[3.0.0]: https://github.com/MetaMask/eth-sig-util/compare/v2.5.4...v3.0.0
[2.5.4]: https://github.com/MetaMask/eth-sig-util/compare/v2.5.3...v2.5.4
[2.5.3]: https://github.com/MetaMask/eth-sig-util/releases/tag/v2.5.3

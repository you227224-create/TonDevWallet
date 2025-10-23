363240aff0185a5593cb828a19cd6dfaceb8bc6c# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.7.2] - 2025-07-08

### Fixed
- Updated dependencies to support new TON updates

## [0.7.1] - 2025-06-14

### Added
- Custom Toncenter API URL setting
- Option to use BIP-39 mnemonics (Tonkeeper-style)
- Automatic interception of TonConnect QR-codes from clipboard and images
- Interface and UI for `signData` TonConnect requests, including MessageRowSign component
- Pagination and progress indicator for transaction history
- "valid until" check for pending messages on the home screen
- Allow sending transactions with hex-encoded body
- Explorer URL now derived from the currently selected network

### Fixed
- Unhandled exception when `jettonOwnerAddr` is not resolved in transaction tracer
- Error thrown for transactions without a compute phase
- Duplicate messages when the browser extension is connected to the same wallet as the dApp
- Incorrect SVG child node limit inside the browser extension

### Technical
- Updated `@tondevwallet/traces` package to drop `@ton/core` & `Buffer` peer requirement

## [0.7.0] - 2025-04-13

### Added
- Browser extension that intercepts TonConnect transactions in browsers and sends them to the app for emulation
- `@tondevwallet/traces` library for developers to easily send traces to the TonDevWallet
- Mode selection for sending transactions with customizable flags (pay fees separately, ignore errors, bounce on fail, etc.)
- Enhanced tracer page with tab support for multiple trace analysis sessions

### Fixed
- Public key encoding issues when importing view-only wallets

### Technical
- Migrated codebase to Tauri 2.0 framework

## [0.6.2] - 2025-04-06

### Added
- Discovery of wallets with balances for known keys and new ones
- Support for address input in new read-only wallet creation

### Fixed
- Stack parsing error that caused unhandled exception in some cases

## [0.6.0] - 2025-04-02

### Added
- Support for extra currency in transfers
- TLB/Cell parser utility functions
- Ton unit formatting utilities
- Transaction retracer utility for blockchain transaction analysis

### Fixed
- Improved support for view-only wallets

## [0.5.0] - 2024-02-17

### Added
- Support for saving emulation traces and viewing them in the app
- Show shards in transaction emulation preview
- Search for wallets by name in tonconnect popup

### Fixed
- Patched @ton/core to parse anycast address

## [0.4.6] - 2025-02-10

### Added
- Workchain ID selection (basechain (0) or masterchain (-1))
- Support for v1, v2 and v3R1 wallet versions

## [0.4.5] - 2024-12-13

### Added
- W5 wallet support with subwallet ID handling
- Basic transaction ABI parser
- Automatic library loader for contract execution

### Fixed
- Empty balance display for contracts without state
- Error handling for invalid TonConnect payloads

### Updates
- Added timeout to highload v3 wallets

## [0.4.4] - 2024-05-07

### Updates
- Rewritten ui to use shadcn/ui
- HighloadV2R2 support
- HighloadV3 support
- MultisigV2 support
- Added custom network selector
- Improve network connectivity and reconnects

## [0.4.3] - 2023-12-15

### Updates
- Added new SendTransaction feature with maxMessages to tonconnect.
- Fixed empty name saved for new wallet from random generation.
- Wallet list now respects testnet flag for addresses.
- Transaction emulation preview now has a different background for testnet.

## [0.4.2] - 2023-07-28

### Added
 - Add option to automatically approve and send any message from selected session.
 - Change app name in TonConnect event to `tonkeeper`.

## [0.4.1] - 2023-07-15

### Added
 - Refactor login popup.
 - Remember last used wallet for website.
 - Allow to paste tonconnect links anywhere to initiate session.
 - Add fallback in case manifest cannot be reached.

## [0.4.0] - 2023-07-13

### Added
 - Move QRCode parser to rust side.
 - Allow to paste images of qrcodes to initiate tonconnect.
 - Bring to front on transactions and login attempts.
 - Fix no login screen on first start.

## [0.3.9] - 2023-05-27

### Added
 - Stack Trace Viewer for Emulated Transactions. Now you can view stack trace for transactions.
 
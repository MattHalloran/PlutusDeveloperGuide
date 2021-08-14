# Plutus Development Guide
The goal of this repository is to be a single resource for development with Plutus. It covers:
- Setting up the Plutus Playground,
- Plutus Pioneers resources, with homework solutions
- Alonzo testnet and exercises
- Alternatives to Plutus development

## Quick Links
- [Cardano main resource guide](https://github.com/MattHalloran/CardanoResources)

## Plutus Pioneers Program
- [Plutus Playground website](https://playground.plutus.iohkdev.io/) (**VERY OUTDATED**)
- [Installation](docs/PlaygroundInstall.md)
- [Lectures: YouTube](https://www.youtube.com/channel/UCcAwSpbpQDDzEDRQqcDH8Iw/videos)
- [Lecture guide: ReadTheDocs](https://plutus-pioneer-program.readthedocs.io/en/latest/plutus_pioneer_program.html)
- [Cohort 1 class photo](https://pool.pm/d068fe47123ec4c86460eeb74c7d7765c67d2df295a3ac86d664ed45.PlutusFirstClassPhoto288)

## Alonzo testnet
- [Easiest installation (in my opinion): Docker](https://docs.cardano.org/getting-started/installing-the-cardano-node)
- [Creating and funding test wallet]()
- [Exercises and resources](https://github.com/input-output-hk/Alonzo-testnet)
- [Alonzo walkthrough: ReadTheDocs](https://plutus-pioneer-program.readthedocs.io/en/latest/alonzo.html)

## Lectures

- [Lecture #1](https://youtu.be/IEn6jUo-0vU)

  - Welcome
  - The (E)UTxO-model
  - Running an example auction contract on a local Playground
  - Homework

- [Lecture #2](https://youtu.be/E5KRk5y9KjQ)

  - Triggering change.
  - Low-level, untyped on-chain validation scripts.
  - High-level, typed on-chain validation scripts.

## Code Examples

- Lecture #1: [English Auction](code/week01)
- Lecture #2: [Simple Validation](code/week02)

## Exercises

- Week #1

  - Build the [English Auction](code/week01) contract with `cabal build` (you may need to run `cabal update` first).
  - Clone the [The Plutus repository](https://github.com/input-output-hk/plutus), check out the correct commit
    as specified in [cabal.project](code/week01/cabal.project).
  - Set-up IOHK binary caches [How to set up the IOHK binary caches](https://github.com/input-output-hk/plutus#iohk-binary-cache). "If you do not do this, you will end up building GHC, which takes several hours. If you find yourself building GHC, STOP and fix the cache."
  - Enter a `nix-shell`.
  - Go to the `plutus-playground-client` folder.
  - Start the Playground server with `plutus-playground-server`.
  - Start the Playground client (in another `nix-shell`) with `npm run start`.
  - Copy-paste the auction contract into the Playground editor - don't forget to remove the module header!
  - Compile.
  - Simulate various auction scenarios.

- Week #2

  - Fix and complete the code in the [Homework1](code/week02/src/Week02/Homework1.hs) module.
  - Fix and complete the code in the [Homework2](code/week02/src/Week02/Homework2.hs) module.

## Some Plutus Modules

- [`PlutusTx.Data`](https://github.com/input-output-hk/plutus/blob/master/plutus-tx/src/PlutusTx/Data.hs), contains the definition of the `Data` type.
- [`PlutusTx.IsData.Class`](https://github.com/input-output-hk/plutus/blob/master/plutus-tx/src/PlutusTx/IsData/Class.hs), defines the `IsData` class.

## Additional Resources

- [The Plutus repository](https://github.com/input-output-hk/plutus)
- [Learn You a Haskell for Great Good!](http://learnyouahaskell.com/)
- [Haskell & Cryptocurrencies course Mongolia](https://www.youtube.com/playlist?list=PLJ3w5xyG4JWmBVIigNBytJhvSSfZZzfTm)

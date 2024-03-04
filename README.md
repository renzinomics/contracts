# Ecosystem NFT Contracts

This project represents the smart contracts used for the Superfluid NFT Ecosystem Rewards Pass mint as seen [here](https://mint.superfluid.finance/). The smart contracts use Superfluid's Distribution Pools in order to assign a share in a pool to all the minters.

## How does it work?

Each time a user mints an NFT, a share (unit) is assigned to that user at a Superfluid Distribution Pool on the blockchain. At the same time, the stream period is extended to end at a month from that last mint. This might make the total flow rate a bit bigger or smaller for the whole Pool, but always makes the flow rate a bit smaller for each member unit (share) in the Pool. However the stream keeps going for a longer period to compensate for that.


## Usage

### Install

```shell
$ forge install
```

### Build

```shell
$ forge build
```

### Test

```shell
$ forge test
```

_PS: If you are having trouble running `forge build` and `forge test` because of `stack too deep` error, this is normal as the tests deploy the whole Superfluid Framework. You can get around that by using [the Yul Optimizer](https://docs.soliditylang.org/en/latest/yul.html) by adding the flag --via-ir._

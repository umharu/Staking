## Foundry

**Foundry is a blazing fast, portable and modular toolkit for Ethereum application development written in Rust.**

Foundry consists of:

-   **Forge**: Ethereum testing framework (like Truffle, Hardhat and DappTools).
-   **Cast**: Swiss army knife for interacting with EVM smart contracts, sending transactions and getting chain data.
-   **Anvil**: Local Ethereum node, akin to Ganache, Hardhat Network.
-   **Chisel**: Fast, utilitarian, and verbose solidity REPL.

## Documentation

https://book.getfoundry.sh/

## Usage

### Build

```shell
$ forge build
```

### Test

```shell
$ forge test
```

### Format

```shell
$ forge fmt
```

### Gas Snapshots

```shell
$ forge snapshot
```

### Anvil

```shell
$ anvil
```

### Deploy

```shell
$ forge script script/Counter.s.sol:CounterScript --rpc-url <your_rpc_url> --private-key <your_private_key>
```

### Cast

```shell
$ cast <subcommand>
```

### Help

```shell
$ forge --help
$ anvil --help
$ cast --help
```
# Staking
Para poder realizar el test las hay que tener en cuenta las siguiente consideraciones:

- La siguiente variables del archivo staking.sol deben cambiar de private a public:

// Variables que corresponden al owner
uint256 private contractBalance;
address private immutable owner;

// Variables almacenan el tiempo permitido por stake
uint256 private oneYearStakeTimeStamp;
uint256 private twoYearStakeTimeStamp;
uint256 private threeYearStakeTimeStamp;

// Variables almacenan la recompensa segun el año
uint256 private rewardForOneYear;
uint256 private rewardForTwoYear;
uint256 private rewardForThreeYear;

- La función parseNumberToSeconds debe ser public en lugar de internal.
- La función rewardCalculated debe ser public en lugar de internal.



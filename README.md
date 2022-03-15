# L2 AAVE rewards

A staticAToken bridge to Starknet for cheap AAVE rewards collection and token
exchange.

## Architecture

<!-- insert architecture image -->

## Testing

The project is tested using [hardhat](https://hardhat.org/), the [starknet
hardhat plugin](https://github.com/Shard-Labs/starknet-hardhat-plugin),
[starknet-devnet](https://github.com/Shard-Labs/starknet-devnet), and
[ganache](https://trufflesuite.com/ganache/index.html).

### Prerequisites

Before installing cairo you'll need to install GMP

```bash
sudo apt install -y libgmp3-dev # linux
brew install gmp # mac
```

```bash
nvm install 16

python3.7 -m venv .venv
source .venv/bin/activate
pip install cairo-lang starknet-devnet
```

### Start the testnets

It's wise to do this in two separate shells

```bash
yarn hardhat node
```

```bash
starknet-devnet
```
### Build the cairo files

```bash
yarn hardhat starknet-compile
```

### Run the tests

```
yarn test
```

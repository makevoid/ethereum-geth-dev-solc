# Ethereum DEVnet Container

One geth node, based on Ubuntu 16.04 LTS

(changes from the original makevoid/ethereum-geth-dev container: includes **solc** - Ethereum contract Solidity compiler)

#### Features:

- Automatic address generation (generates a new coinbase address)
- Genesis block setup (low difficulty for quick tx confirmations, high gas block limit)
- Mining script (starts mining only when new transactions are present)

### Usage:

    docker pull makevoid/ethereum-geth-dev-solc 
    docker run -p 8545:8545 makevoid/ethereum-geth-dev-solc


It also has:

- Node JS
- Web3 as npm module
- Coffeescript

If you want a password different than `foo` please edit `config/password.txt` before running :D, also you'll may want to not automatically unlock the address via the geth `--password` arg/flag.

Please take a look at the Dockerfile, it's quite simple and has few options (logging of some steps, regenerating the address...)


Enjoy,

@makevoid

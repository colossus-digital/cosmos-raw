<h1 align="center">
    <b>cosmosRaw</b>
</h1>

<p align="center">
  <a href="https://pypi.org/project/cosmosRaw/">
    <img alt="PyPI" src="https://img.shields.io/pypi/v/cosmosRaw">
  </a>
  <a href="https://pypi.org/project/cosmosRaw/">
    <img alt="PyPI - Python Version" src="https://img.shields.io/pypi/pyversions/cosmosRaw">
  </a>
  <a>
    <img alt="PyPI - Wheel" src="https://img.shields.io/pypi/wheel/cosmosRaw">
  </a>
  <a href="https://github.com/fetchai/cosmosRaw/blob/master/LICENSE">
    <img alt="License" src="https://img.shields.io/pypi/l/cosmosRaw">
  </a>
</p>
<p align="center">
  <a href="https://github.com/fetchai/cosmosRaw/actions/workflows/workflow.yml">
    <img alt="AEA framework sanity checks and tests" src="https://github.com/fetchai/cosmosRaw/actions/workflows/workflow.yml/badge.svg">
  </a>
  <a href="https://github.com/fetchai/cosmosRaw/actions/workflows/workflow.yml">
    <img alt="Contributor Covenant" src="https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg">
  </a>
</p>

<p align="center">
A python library for interacting with cosmos based blockchain networks
</p>

## Installing

To install the library use:

```bash
pip3 install cosmosRaw
```

## Getting Started

Below is a simple example for querying an account's balances:

```python
from cosmosRaw.aerial.client import LedgerClient, NetworkConfig

# connect to Fetch.ai network using default parameters
ledger_client = LedgerClient(NetworkConfig.fetchai_mainnet())

alice: str = 'fetch12q5gw9l9d0yyq2th77x6pjsesczpsly8h5089x'
balances = ledger_client.query_bank_all_balances(alice)

# show all coin balances
for coin in balances:
    print(f'{coin.amount}{coin.denom}')
```

## Documentation

Before running this command make sure your development environment is set up. Check [Development setup](DEVELOPING.md#development-commands) for more details.

To see the documentation:

```bash
make docs-live
```

Then navigate to the following URL in your browser:
<!-- markdown-link-check-disable-next-line -->
[http://127.0.0.1:8000/cosmosRaw/](http://127.0.0.1:8000/cosmosRaw/)

## Examples

Under the `examples` directory, you can find examples of basic ledger interactions using `cosmosRaw` e.g. transferring tokens, staking, deploying and interacting with a smart contract, and performing atomic swaps.

## To contribute

Please see [CONTRIBUTING](CONTRIBUTING.md) and [DEVELOPING](DEVELOPING.md) guides.

## Extra Resources

* [Github Repo](https://github.com/fetchai/cosmosRaw)
* [Bug Reports](https://github.com/fetchai/cosmosRaw/issues)
* [Discussions](https://github.com/fetchai/cosmosRaw/discussions)
* [Getting Started](https://docs.fetch.ai/cosmosRaw/)

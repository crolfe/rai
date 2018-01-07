# ⛓ rai

**rai** is a high-level client for interacting with [Raiblocks](https://raiblocks.net/) nodes.

## Install

pip install rai

## Usage example

```python
from rai import Wallet


wallet = Wallet(id='4A84E2353EA3F363094EC7844A33B395E2BFDFCE19506FAFC37C73E7653D430F')
print(wallet.total_balance)
# 2500000000
print(wallet.accounts)
# ['xrb_3e3j5tkog48pnny9dmfzj1r16pg8t1e76dz5tmac6iq689wyjfpi00000000', xrb_dmfzj1r16pg3e3j5tkog48pnny98t1e76dz5c6iq689wyjfpitma00000000, 'xrb_mac6iq6x1r16pg8t1e76dz5t89wyjfpmac6iq6r00000000']
block = wallet.send(
    source='xrb_3e3j5tkog48pnny9dmfzj1r16pg8t1e76dz5tmac6iq689wyjfpi00000000',
    destination='xrb_3e3j5tkog48pnny9dmfzj1r16pg8t1e76dz5tmac6iq689wyjfpi00000000',
    amount='1000000'
)
print(block)
# 000D1BAEC8EC208142C99059B393051BAC8380F9B5A2E6B2489A277D81789F3F
```
# SKY Token and contract associated

This repository includes 2 smart contracts:

- SKY token
- MkrSky Converter

### MkrSky

It is a converter between `Mkr` and `Sky` (both ways). Using the `mint` and `burn` capabilities of both tokens it is possible to exchange one to the other. The exchange rate is 1:`rate` (value defined as `immutable`).

**Note:** if one of the tokens removes `mint` capabilities to this contract, it means that the path which gives that token to the user won't be available.

**Note 2:** In the MKR -> SKY conversion, if the user passes a `wad` amount not multiple of `rate`, it causes that a dusty value will be lost.

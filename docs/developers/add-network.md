# Adding a Network to Core-Geth

CoreGeth currently supports a handful of networks out of the box, 
and can readily be configured to support others.

This guide will show you how to add a network to CoreGeth.

For the context of this tutorial, I'm going to use __AlphaBeta Coin__:registered:
as the name of my new network. 
 - AlphaBeta Coin (ABC) will use Proof-of-Work for block issuance, 
   namely ETHash. (Just like Ethereum.)
 - AlphaBeta Coin will have some arbitrary pre-mine funds allocated to a few addresses.
 - AlphaBeta Coin will have the "Istanbul" (aka "ETC's Phoenix") protocol upgrades and
   EVM features activated from genesis.
   

### Define the Configuration

Tag: `docs.tutorial-add-network.establish-chain-config`

```
$ git --no-pager diff --name-only v1.11.22
docs/developers/add-network.md
params/bootnodes_abc.go
params/config_abc.go
params/config_abc_test.go
params/genesis_abc.go
```

2233ec80cb writes an Example test showing and validating the
JSON encoding of our new configuration.


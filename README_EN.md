
### Reconstruct the Test Network


At present, the minimum version required for the test network is the mainnet force-v1.7.1 version. It is recommended to use the latest version on Github which is compiled from the latest code.


Test network root node P2P address: 147.52.71.18：10000


This address will be closed after the test network startup


### Start Compile

This is similar to the main net startup. It should be noted that the genesis file required for the test network startup is different from the mainnet.

Start Command: ./nodeos --config-dir=./config --data-dir=./data

### The Original Test Network Startup Process


1.Replace config

Replace genesis.json in the config folder with the original genesis.json. For config.ini file, you can use the config.ini file in the folder, or you can change p2p-peer-address address to p2p-peer-address = 47.52.71.18:10000

2.Select an empty data folder to start the node

Use the command ./nodeos --config-dir=./config --data-dir=./data to start the node

###3.Create BP account


You can send the public key to the development team to create an account. The development team will transfer test tokens to the new account to invoke the function of the test network.

producer-name = BPBANE
signature-provider = Public key=KEY:Private Key


Restart the node as the block-producing node

**You can configure 2 producer-name and signature-provider, which means that one node can be used as a program of 2 BPs.**
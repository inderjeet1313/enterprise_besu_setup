# enterprise_besu_setup

## Steps

1. Create the directories
2. Download the Besu and set the bin folder in environment variable path
3. Create the network_configuration.json file
4. Generate node keys and genesis file using the command:

`besu operator generate-blockchain-config --config-file=network_configuration.json --to=networkFiles --private-key-file-name=key`

5. The above command will create a new folder networkFiles and put all the keys and genesis file there
6. Move the genesis file to the root folder
7. Each folder inside keys folder represents Node keys. In this case, there are 10 folder with node keys. Move these to data folder that were created earlier. Each set of keys are for individual nodes.
8. For each node, generate the node address. Run the following command in all the data folders:
   `besu public-key export-address --to=node_address --node-private-key-file=key`
9.  We need to generate the static enode addresses for the nodes. For this, we need to start each node one by one, copy the enode url from the console.

## End points

### Archival Node 
- RPC: 8081
- WS: 7071
- P2P: 30301

### BootNodes
#### BootNode1
- P2P: 30302

#### BootNode2
- P2P: 30303

#### BootNode3
- P2P: 30304

### RPC Node
#### RPC Node 1
- RPC: 8082
- WS: 7072
- P2P: 30305

### Validators
#### Validator 1
- RPC: 8083
- P2P: 30306

#### Validator 2
- RPC: 8084
- P2P: 30307

#### Validator 3
- RPC: 8085
- P2P: 30308

#### Validator 4
- RPC: 8086
- P2P: 30309

#### Validator 5
- RPC: 8087
- P2P: 30340

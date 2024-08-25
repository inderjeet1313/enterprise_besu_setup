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
8. We need to generate the static enode addresses for the nodes. For this, we need to start each node one by one, copy the enode url from the console.

# electrs with bitcoind

## Run

`docker-compose up --build`

## Call electrs APIs

1. connect elements container
`docker exec -it bitcoind /bin/bash`

2. generate block where n is the number of blocks to generate
`bitcoin-cli -regtest -rpcuser=johnny -rpcpassword=mnemonic generate n`

3. call API
`curl http://localhost:3002/blocks/tip/hash`

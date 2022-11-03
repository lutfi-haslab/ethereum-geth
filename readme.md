command create account
```bash 
geth --datadir "./data" account new
```
## Consensus Used
Proof of Authority

## node1
pw: perurinode1
Public address of the key:   0x38C008b4c70496656Eb1f7FfB87F284c8Aa1c1b1

## node2
pw: perurinode2
Public address of the key:   0xa707b3C183593154b1674216bA451543b615a9ad

chain id: 2102
path configuration: C:\Users\prifalab\.puppeth

start the network
```bash
node1>> geth --datadir ./data init ../blockpoa.json
node2>> geth --datadir ./data init ../blockpoa.json
```

$ puppeth
+-----------------------------------------------------------+
| Welcome to puppeth, your Ethereum private network manager |
|                                                           |
| This tool lets you create a new Ethereum network down to  |
| the genesis block, bootnodes, miners and ethstats servers |
| without the hassle that it would normally entail.         |
|                                                           |
| Puppeth uses SSH to dial in to remote servers, and builds |
| its network components out of Docker containers using the |
| docker-compose toolset.                                   |
+-----------------------------------------------------------+

Please specify a network name to administer (no spaces, hyphens or capital letters please)
> blockpoa

Sweet, you can set this via --network=blockpoa next time!

INFO [11-03|10:28:00.403] Administering Ethereum network           name=blockpoa
WARN [11-03|10:28:00.403] No previous configurations found         path=C:\Users\prifalab\.puppeth\blockpoa

What would you like to do? (default = stats)
 1. Show network stats
 2. Configure new genesis
 3. Track new remote server
 4. Deploy network components
> 2

What would you like to do? (default = create)
 1. Create new genesis from scratch
 2. Import already existing genesis
> 1

Which consensus engine to use? (default = clique)
> yes

Specify your chain/network ID if you want an explicit one (default = random)
> 2102
INFO [11-03|10:29:47.241] Configured new genesis block

What would you like to do? (default = stats)
 1. Show network stats
 2. Manage existing genesis
 3. Track new remote server
 4. Deploy network components
> 2

 1. Modify existing configurations
 2. Export genesis configurations
 3. Remove genesis configuration
> 2

Which folder to save the genesis spec into? (default = current)
  Will create blockpoa.json
> blockpoa.json
INFO [11-03|10:34:13.830] Saved native genesis chain spec          path=blockpoa.json\blockpoa.json

What would you like to do? (default = stats)
 1. Show network stats
 2. Manage existing genesis
 3. Track new remote server
 4.

 exit

untuk menghubungkan antar peers, maka diperlukan bootnode:
command nya adalah :
```bash
bootnode> bootnode -genkey boot.key
```
lalu buat koneksi menggunakan enode berikut:
```bash
enode://cec73c8607b412e58f05b4032299e2610e67214fbad1891fc2f10d6b9cba0125600411c70cc8e1aa650b0cfcae8ec838ef3b3402d86cb806298e138bdb78c6b5@127.0.0.1:0?discport=30301
```

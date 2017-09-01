# Overview 
This script is to be used in the geth console to get the information in a blockchain

#Usage 
1. Open geth console connecting to your node rpc/ipc address. For example, if the default geth node port is 8545, type `geth attch http://localhost:8545` to connect to the node and open geth console
2. In geth console, type `loadScript('path_of_this_script')` to load this script. It will return true if the script is loaded successfully
3. As defined in the script, run `init()` for intitialization and then run `getInfo()` to get the blockchain information. Everytime the blockchain is updated, run `getInfo()` again to retrieve the lastest data.

# Data that can be retrieved: 
1. blocks: an array containing info of all current blocks 
2. gasUsed: total gas used by now
3. tnxHashes: an array containing all transaction hashes
4. totalDifficulties: an array of the mining difficulty of each block
5. emptyBlockNum: the number of empty blocks (blocks with no transactions)
6. blockMiningTime: the time between each block is mined in seconds 
7. tnxReceipts: an array of all transaction info (The `from` and `to` addresses will be undefined if the transaction is not a standard `sendTransaction`)
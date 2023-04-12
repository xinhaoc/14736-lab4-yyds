# 14736-lab4-yyds
Lab4 proposal

## selected option:
Option IV: Implement Proof-of-Work Blockchain Consensus
## high-level description:
The system is a distributed implementation of the POW algorithm for blockchain consensus.  
System high-level functions:  
Peers will automatically generate new transactions, the transactions will be broadcasted to all peers in the system, the one who first validates the transaction will add the new block and get a mining reward.
We will use rpc as a remote call library, and also a byzantine fault-tolerant consensus mechanism.
## design requirements:
To achieve this system requirement, we need some core components:
* a consensus manager to manage the clients status, includes their local entries(block chain objects)
* a function to calculate the pow using SHA-256, prove whether the received object is a valid block chain.
* a function to calculate a new transactions and append to the previous block chain
* a function to reward the client who “mine” the new block
## approach:
* We will create a remote library from PRC call, an application library for validation/mine in blockchain, and a consensus library for managing clients status.
* We will use Java as the programming language of our work. 
* We will need some third party packages:
java.io.ByteArrayOutputStream for reading from the encoded bytes in blockchain
java.util.Base64 for network encoding/decoding
org.json.JSONObject and org.json.JSONArray to read from the json format string in blockchain requests
java.net.* from read/write from socket
java.lang.reflect.Method, java.lang.reflect.Type from RPC reflections
## test cases:
* Block chain tests: bad timestamps order, bad hashing, mismatched blockid, etc.
* Consensus tests: leader election, leader reelection, peer failure, peer majority failure, etc.
* Content tests: idempotent




# Scrooge Coin
* In this project, we will design a cryptocurrency similar to ScroogeCoin. 
* A network of **100 users** will simulate the transaction processes. 
* Initially each user will have **10 ScroogCoins.** 
* As long as the system is running, a random transaction with random amount **(within the range of amount the user has)** will be created from User A to User B. 
* The transaction is **signed by the private-key of the sender.**
* Scrooge get notified by every transaction. 
* Scrooge **verifies the signature** before accumulating the transaction. 
* Once Scrooge **accumulates 10 transaction**, he can form a block and attach it to the blockchain.
* Dependencies: 
    - ecdsa is used for signing.
    - sha256 is used for hashing.
* A designated entity “Scrooge” publishes an append-only ledger that contains all the history of transactions.
* The ledger is a blockchain, where each block contains transactions, its ID, the hash of the block, and a hash pointer to the previous block. The final hash pointer is signed by Scrooge.
* A simulation of the network, with multiple users and the randomized process of making a transaction, making each transaction reach an arbitrary user.
* The design and implementation of the ledger based on the concept of the
blockchain (hash linked list).
* Upon detecting any transaction, scrooge verifies it by making sure the coin really belongs to the owner and it has not been spent before.
* If verified, Scrooge adds the transaction to the blockchain. Double spending can only happen before the transaction is published.

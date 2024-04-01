# Distributed_Cryptocurrency_System
Imagine there are a bunch of parties, and they should agree on a value V. V is the ledger that says how much money everyone has, e.g., a list of transactions. 
In a non-distributed system, a centralized organization, like a central bank would propose the ledger. But the problem is that the bank has full control, and everything relies on only one party which makes it hard to trust. The bank can change the ledger and fake a transaction for its own profit or other corrupted individuals.
To solve this problem, we need to detect if the bank has changed any of the transaction histories. Another solution is using a digitally distributed system, where every one of the parties has control over the network and transactions are transparent for everybody and they can validate them. But since it’s a digital transaction and not physical cash, we’ll face another problem called double spending. Double spending is spending the same single digital token more than once, and a digital token can be duplicated or falsified.
Bitcoin was the first digital currency that made a distributed system work perfectly by solving decentralization and double spending.
 
 
 
These are the steps done to simulate a distributed cryptocurrency system on a small network:

1.	We created a peer-to-peer network with 10 participants. Each participant is considered as a node and they are connected to other nodes with edges, such that the whole network is connected through each other, a connected graph. Our imaginary P2P network graph:
 
 
 
 
Fig: P2P Network
 

 
2.	For each participant, a private key, public key, and an adjacency list has been provided. With their private key, we generated a signature for them to be used for transactions.
 
3.	Each block consists of a hash pointer, transactions and their hashes, nonce, and public key.
 
4.	All the steps needed for adding, mining, broadcasting, and validation of blocks are implemented in the fourth section. Mining new blocks requires the difficulty problem to be solved. It starts by a nonce equal to zero and passes its generated hash and the transaction to the add block function. Next, we check to see if the nonce hash is smaller than the difficulty value, if yes then we have a new block. If no, then the nonce gets increased for the next round and it goes on and on till we have a solution.
After mining a new block, we must broadcast to all the neighbors and they must validate whether the block’s position would make the main chain longer or not, and other winners of the mining difficulty would get rejected for placing their block in the chain. And of course, all the participants need to check the whole procedure and validate new block.
After every transaction, we broadcast it to all the individuals in the network, compare if they have the transaction in their block, if not we add it to theirs. 
 
5.	Then we initiate some transactions between participants/ neighbors and mine new blocks for the transactions.
 
6.	Then we simulate five rounds of the whole process, broadcasting new transactions, mining, and broadcasting new blocks and print out the new blocks added to the main chain.
 
 
 
The aim of this project was simulating a distributed cryptocurrency. To answer the distributed part, we designed a P2P network of users and to address the cryptocurrency system, we implemented the code for a simple procedure of tasks needed, including mining, broadcasting, and validation. In the end, to test the network and its functionality, we simulated a few operations of the whole system such as: transaction, mining, broadcast.

![image](https://github.com/mghasemizade/Distributed_Cryptocurrency_System/assets/74173811/21d9c622-096c-4004-b3ca-5c0927c9df26)

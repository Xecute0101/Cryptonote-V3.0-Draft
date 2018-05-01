# CryptoNote-V3.0-Draft

What will be suggested in this paper will be

A. Node Optimization
B. Smart Wallet Function

How to solve issues related to transaction size and blocksize limit causing network noise among nodes:
CryptoNote 2.0 insists organic block size growth over time. However, in real application of this theory, there are limitations because transaction pool receives various type of transactions, which need to be included in a block.

There are four variables that changes the transaction size; amount of coins, # of inputs, # of outputs and mixin count.

Case 1. Large number of coins & Using many digits and decimals
For example, Qwertycoin (QWC) is designed with the maximum coin supply limit of 184.47 billion coins with 8 decimals.
For those transactions with using XXX,XXX.XXXXXXXX is most likely to exceed normal block size limit of the coin.

Case 2. Mixin count
Using high mixin count will cause error messages and the subjected amount of coins will be held in the tranasction pool until it is deleted per coin's core coding.

Case 3. To be Added

Through above cases, nodes will display error such as transaction is too large or mixin count is too big. As more errors are received by multiple wallet sources, the nodes will eventually crash due to high transaction pool size and node's individual processing limit based on its hardware and infrastructure.

A. Node Optimization - Pre Authorization
First we need to preapre a clone blockchain which syncs with the main blockchain. Wallet software will send transaction query to the clone blockchain

If node(s) of clone blockchain approves such format(amount, mixin) of transaction query, wallet software will make the same query to the nodes on the main blockchain. This way, rejects of transactions due to large amount or high mixin can be prevented from reaching nodes working in the main blockchain.

B. Smart Wallet Function - Dividing payment into pieces
Instead of sending a large and complex amount of coins such as XXX,XXX.XXXXXXXX, dividing transaction integers and decimals to optimum sizes will reduce the size of transaction hashspeed and speed up transaction confirmation speed because they will be easier to be included in blocks. 

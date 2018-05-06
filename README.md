# CryptoNote-V3.0-Draft

What will be suggested in this paper will be

A. Egalitarian Proof of Work based on Coin Distribution
B. Egalitarian Proof of Service (PoSe) based on Uptime
C. Node Optimization
D. Smart Wallet Function


A. Egalitarian Proof of Work based on Coin Distribution

A-1.
At the time of Cryptonote V2.0, miners were mainly divided into two types of hardware; CPU and GPU, the latter becoming a threat to the former in terms of hashrate each type of hardware can produce. CPU mining period has phased out as multiple GPU mining rigs became the main stream in CryptoNote mining communities. 

The market for cryptocurrency has advanced in 5 years and, as of January 2018, ASIC mining hardwares were introduced to the CryptoNote mining communities, and they provide significant advantages over GPU mining rigs in terms of hashrate per hardware and electricity costs.

A-2.
The word 'Egalitarian' means all people are equal and deserves 'equal' rights and opportunities. under current mining ecosystem, CPU, GPU and ASIC mining cannot satisfy this egalitarianism concept. Fork effrots to Anti-ASIC mining algorithm have been made by the majority of CryptoNote communities to keep ASIC mining hardware from the network. But this is a type of centralization.

In this paper, I would like to propose Egalitarian Proof of work based on Coin Distribution. Because the emission of a Cryptonote coin is predictable based inherent emission rate designed in the core of each coin, allowing sequential entrance of each mining platform to mining pools at specific points of the emission can provide more 'equal' rights to mine and 'equal' opportunities in terms of earning coins. Also as a result of this action, the coins will have a better distribution among community miners.

[graph and diagram to be added to provide examples]

B. Egalitarian Proof of Service (PoSe) based on Uptime

Wallet platform has also evolved from desktop/laptop computers to mobile devices over time. However, mobile wallet solutions have storage and bandwidth limitations. Because of these limitations, mobile wallet solutions are required to connect to remote daemon in order to synchronize with blockchain and make transactions.

Most coins utilizes Proof of Stake(PoS) concept as the mean of providing interests on staking coins and thereby incentivizing those node operators to hold onto coins instead of trading them in the market. The amount of interests provided to node operator increases based on the number of coins locked into each node account.

In the process of earning coins, either by mining or providing nodes to the network, the same egalitarian concept shall be applied in CryptoNote coins because they are all part of the same ecosystem and they are entitled to receive coins for their work and service. 

The proposed method is to use the concept of Uptime. This method requires one premise that there is no minimum coin requirement to operate a node and it shall be free to join. 

For example, all nodes, which meets the minimum requirement for compensation based on Weighted Uptime, can share accumulated transaction fee per a given time period.

C. Node Optimization

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

B. Node Optimization - Pre Authorization
First we need to preapre a clone blockchain which syncs with the main blockchain. Wallet software will send transaction query to the clone blockchain

If node(s) of clone blockchain approves such format(amount, mixin) of transaction query, wallet software will make the same query to the nodes on the main blockchain. This way, rejects of transactions due to large amount or high mixin can be prevented from reaching nodes working in the main blockchain.

C. Smart Wallet Function - Dividing payment into pieces
Instead of sending a large and complex amount of coins such as XXX,XXX.XXXXXXXX, dividing transaction integers and decimals to optimum sizes will reduce the size of transaction hashspeed and speed up transaction confirmation speed because they will be easier to be included in blocks. 

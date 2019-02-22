# <div align=center>**WHITEPAPER**</div>
### <div align=center></div> 
## <div align=center>More Safety Crypto Currency</div>
### <div align=center>v1.0</div>
### <div align=center>**Github**:[https://github.com/wabei](https://github.com/wabei)</div>

### <div align=center>2018年7月</div>  

<!-- TOC -->

## 目录
- [Index](#Index)
- [一、Potential Risks with Bitcoin](#1-Potential Risks with Bitcoin)
    - [1.1 Bitcoin Mining](#11-Bitcoin Mining)
    - [1.2 Centralization of Hash Power](#12-Centralization of Hash Power)
    - [1.3 Loss of Private Key ](#13-Loss of Private Key)
- [二、Double Block Chains ](#2-Double Block Chains)
    - [2.1 ](#21-Pain Points in IT Infrastructure in Financial Industry)
    - [2.2 Mining](#22-mining)
    - [2.3 Restriction of Pool Mining](#23-Restriction of Pool Mining)
    - [2.4 Wabash Engine](#24-Security Engine)
- [三、Wallet](#3-token-S wallet)
    - [3.1 Smart Security Check](#31-Smart Security Check)
    - [3.2 Multisig](#32-Multisig)
    - [3.3 Cold Wallet ](#33-Cold Wallet )
    - [3.4 Secure and Trustworthy Trading Platform](#35-Secure and Trustworthy Trading Platform)
    - [3.5 Quantum Encryption Resistance](#36-Quantum Encryption Resistance)
    - [3.6 Exploration of Quantum Encryption](#37-Exploration of Quantum Encryption)
    - [3.7 One-stop management of multi-chain wallet and currency](#38-One-stop management of multi-chain wallet and currency)
- [四、Other](#4-Other)
    - [4.1 Application ](#41-Application)
    - [4.2 Publisher](#42-Publisher)
    - [4.3 ：Potential Risks with Bitcoin](#43-conclusion：Potential Risks with Bitcoin)
- [About](#About)

<!-- /TOC -->


##Introduction    
Satoshi Nakamoto created Bitcoin and implemented a purely peer-to-peer electronic
cash system. Bitcoin is not backed by any assets nor does it have intrinsic value. It
is not issued by any central government or financial institution. Transactions in the
bitcoin network can be sent directly from one party to another without going
through a financial institution. Bitcoin has the following features:
1. It has no centralized issuer or controller.
2. Transactions can be sent between parties without going through a trusted third
party.
3. A transaction’s originating and receiving parties are anonymous.
4. No transaction can be reversed.
Since bitcoin’s birth it has become the most popular electronic cash system
worldwide. Although it presents a beautiful solution to the double-spending problem
using a P2P network and creates a mechanism to transfer value between trustless
parties over the internet it encounters three significant issues: centralization of hash
power, security concerns with accounts, lost coins can never be retrieved.
The Wabei blockchain is a project that attempts to fix the aforementioned issues.
Among existing permissionless blockchains the biggest issue is centralization of
hash power. Bitcoin’s mining algorithm is based on SHA-256. A block’s eighty-byte
header is hashed twice with SHA-256 to a 256-bit (32-byte) value. It verifies this
block’s validity by comparing this 256-bit value to a nonce. This is known as proof of
work. Although it works well and plays a crucial role it is prone to be attacked by
centralized hash power which means that either large number of nodes can possibly
cooperate to attack the network or a node with an extremely powerful hash rate can
outperform other nodes. For the latter case it already comes true. Nowadays
bitcoin’s mining rigs are nearly all ASIC machines whose efficiency is thousands of
times higher than that of a common desktop computer. Common computers which
were used to mine bitcoins in the early years have been phased out by ASIC
machines. This turns a mining activity into one that needs huge investment.
We think blockchain has huge potentials and is not just an electronic cash system.
Bitcoin’s lack of a Turing-Complete mechanism severely limits its adoption in wider
areas. The Wabei project will be a permissionless blockchain with a Turing-Complete
mechanism on which all transaction-based state machines can be built.
We will analyze several issues the current bitcoin network has in the following
section.  
  
## 一、Potential Risks with Bitcoin 
The concept of decentralized crypto currency was created by Friedrich August von Hayek
in one of his great works << Denationalization of Money >> decades ago. But it is not
until Satoshi Nakamoto who introduced bitcoin this decentralized coin became the
first widely adopted global crypto currency.
Bitcoin’s network is composed of nodes all of which work under a proof-of-work
consensus. Transactions are digitally signed into a block which is generated every
ten minutes. Blocks are chained with hash values to form a blockchain. A node with
a higher hash rate has greater probabilities to mine a block.
Bitcoin is one of the most popular crypto currencies and one of the most robust
blockchain systems.  
    
### 1.1 Bitcoin Mining  
  
In the bitcoin network a block is generated every ten minutes. Every block has a
timestamp, a nonce, a reference (hash value) to its parent block and a list of all
transactions which were completed after the last block in the blockchain. As
ongoing transactions are hashed into the blockchain it will become increasingly
longer. When a block is generated it needs to be verified by all the nodes. It needs
to pass the tests of intrinsic validity. These tests include:
1. Validate its parent block. This examines whether the parent block it is linked to is
valid.
2. Validate its timestamp. A valid timestamp should be greater than its parent
block’s timestamp and less than its parent block’s timestamp plus two hours.
3. Validate its proof-of-work. This examines whether its proof-of-work is valid.
4. Set S[0] to its parent block’s state.
5. Let TX denote a list of transactions and S[i] denote transaction i’s state. We
suppose there are n transactions. For each transaction i in 0......n-1, S[i+1] =
APPLY(S[i], TX[i]). If a transaction fails the system will exit with an error. S[n] is the
final state of the block.
An interesting part of the bitcoin validation mechanism is its proof-of-work. Bitcoin’s
proof-of-work prevents Sybil attacks. Each block is hashed with SHA-256 to a 256-bit
hash value. If this hash value is less than the difficulty value which is dynamically
adjusted by the bitcoin network this block will be a valid block and the bitcoin
system will proceed otherwise the system will keep doing such calculations.
In general the bitcoin network resets the difficulty value every 2016 blocks to
ensure a block is generated every ten minutes. When a block is generated and
chained to its parent block in the blockchain the miner who mined this block will be
rewarded with 12.5 bitcoins. In addition the block’s total transactions’ fee will be
rewarded the miner too.Although this system works it might still face the potential risk of double-spending.
Here is how an attacker might initiate a double-spending attack.
1. Sender sends 100 BTC to receiver A to buy goods or services.
2. Sender waits for delivery of the goods or services.
3. Sender sends 100 BTC to himself right after he gets the goods or services.
4. Sends tries to convince the bitcoin network that the transaction of 100 BTC to
himself happened before the transaction of 100 BTC to receiver A.
We suppose the transaction of 100 BTC to receiver A is hashed to a block and the
block’s height is 270000. One hour later there will be five new blocks (270001 ~
270005) generated after this block. Each of these five blocks will be either directly
or indirectly linked to this block. When receiver A gets 100 BTC he will send the
goods or services to the sender. We suppose what the sender pays for is a digital
item which can be sent immediately from receiver A then right after receiver A gets
100 BTC he will send the digital item and the sender can get it right away. Then
right after the sender receives the digital item he initiates a new transaction to send
100 BTC to his own address. If the sender merely broadcasts the latter transaction
to the bitcoin network in no way can this transaction be hashed into a block
because all miners will eventually find this is an invalid transaction. In order for the
sender to hash this transaction in a block he needs to fork the original blockchain at
height 269999 and generate a new block after the 269999 th block and this new
block will be the 270000 th block in the forked chain. We suppose all honest miners
will generate new blocks either directly or indirectly pointing to the 270005 th block
in the original blockchain and only the sender (attacker) will generate a new block
pointing to the 269999 th block in the forked blockchain. Up to this point the length of
the forked chain is shorter than the original chain. In the bitcoin network the longest
chain is considered the only valid blockchain. Therefore if the sender wants to make
his forked chain the valid chain he has to make his forked chain surpass the original
chain on which all honest miners work. Hence the sender has to have at least 51%
of the bitcoin network’s hash power.  
    
### 1.2 Centralization of Hash Power  
  
Bitcoin’s price has risen tremendously since its birth. This has made bitcoin mining
a huge business with rich profit. The mining business directly drives rapid
development of ASIC rigs which gradually phase out general computers and GPU
machines in this area. On the other hand in order to gain higher probabilities to
mine bitcoins massive individual nodes began to cooperate and have formed big
mining pools therefore individual mining can hardly compete with pool mining
nowadays. It is estimated that the top three mining pools in the world altogether
control 48% of the whole bitcoin network’s hash power.
It is observed that in November 2013 the mining pool GHash.io launched multiple
attacks on BetCoin Dice. A report released by Cornel University reveals that since
June 3 2014 GHash controlled 51% of the whole bitcoin network’s hash power for at
least five times during one of which it had this hash power for at least 12 hours.   
   
### 1.3 Loss of Private Key  
  
A bitcoin address is a string that consists of 34 characters. Every address has a
private key that consists of 64 characters. A bitcoin holder possesses a private key
to his bitcoin address. The private key needs to be carefully stored. If the private
key is lost all the bitcoins stored in the address will be permanently lost. When a
bitcoin holder sends his bitcoins to another address he will need the private key to
authenticate the transaction.
A hacker usually uses keylogger programs, malware or Trojan programs to steal a
bitcoin holder’s private key. It becomes harder to prevent a system from being
infected by these programs in a globally interconnected network.
Statistics reveal that there are nearly two million bitcoins stolen so far, which
accounts for 9.5% of the total number of bitcoins. And this number keeps going up.
The latest incident happened in April 13 2018 when hackers stolen 438 bitcoins
($3.3 million) from an Indian exchange, Coinsecure.  
  
## 二、Double Block Chains 
  
We propose a more secure and decentralized electronic cash system, known as
Wabei. A significant improvement of this project is that it circumvents centralization
of hash power which increasingly becomes a common trend for nearly all PoW
based permissionless blockchains.  
   
### 2.1 Pain Points in IT Infrastructure in Financial Industry  
  
In the Wabei system an account consists of 20 bytes and it comprises the following
fields:
1. nonce: a counter used to make sure each transaction can only be processed
once.
2. balance: an account’s current balance of Wabei coins.
3. contract code: the account’s contract code, if present.
4. storage: the account’s storage. It is empty by default.
The Wabei coin is the internal crypto-fuel of the Wabei system. There are two types
of accounts: external accounts (controlled by private keys) and contract accounts
(controlled by contract code). An external account doesn’t have code. One can send
messages from an external account by creating and signing a transaction. When a
contract account receives a message call the code it contains will get activated and
the code is allowed to read and write to internal storage and send other messages
or create contracts in turn.  
  
### 2.2 Mining 
  
The happness system inherits a lot of features from the bitcoin system but it has
significant differences. A Wabei block has a field known as “block number” and a
field known as “difficulty”. The process of finalizing a block in the Wabei network
involves four stages:
1. Validate its parent block to which this block is linked.
2. Validate the timestamp. It should be greater than its parent block’s timestamp
but less than its parent block’s timestamp plus fifteen minutes.
3. Validate the block number, difficulty, transactions root, uncles root and gas limit.
4. Validate proof-of-work.
5. Set S[0] to its parent block’s STATE_ROOT.
6. Set TX to the block’s transaction list. Suppose there are n transactions, for each
transaction i in 0 ... n-1 set S[i + 1] = APPLY(S[i], TX[i]). If any transaction’s state
change fails or the consumed gas exceeds the GASLIMIT the system will return with
an error.
7. Set S[n] to S_FINAL and apply rewards to a beneficiary.8. Verify if S_FINAL is equal 
to STATE_ROOT. If the two are equal the block is valid.otherwise the block is invalid.
This validation process keeps and examines a block’s all states and doesn’t seem
efficient. But actually the Wabei’s finalization process is as efficient as bitcoin’s
because all states are saved in a tree structure and when a new block is generated
only minor changes will be applied to the tree structure. Therefore most of a block’s
data is the same as its parent block and it is unnecessary to save a copy of every
block’s complete data. A “Patricia Tree” structure is introduced to the Wabei system
to store all the blocks’ data and this greatly saves storage.  
  
### 2.3 Restriction of Pool Mining  
  
Bitcoin mining is prone to be attacked by ASIC rigs and pool mining. Nowadays
nearly all mining machines are ASIC rigs. Common desktops or machines with GPU
in no way can compete with ASIC rigs. It is nearly impossible for individual miners to
mine any bitcoins either. Most of individual miners have to join a pool which collects
individual miners’ hash power and tremendously increases the probability of
successful mining. It is estimated that the top three bitcoin mining pools altogether
control 48% of the bitcoin network’s hash power. All these facts show a de facto
trend: the bitcoin network’s hash power is being centralized. And this trend can
hardly be reversed.
In the Wabei system a hash value is generated based on one thousand random
numbers. This algorithm restricts an ASIC rig’s advantages. In short a Wabei node
needs to utilize large amounts of RAM to mine coins while a bitcoin node doesn’t
need this much RAM thus making an ASIC rig much more efficient in mining. With
this design a common desktop or laptop can run as a full Wabei node and be able to
mine coins. Even when there exists a Wabei node with an extremely large hash rate
a common computer still has good chances to mine coins successfully as long as
the system’s reward is less than (E + H)/E. In addition the mining algorithm requires
a Wabei node to traverse the whole Wabei blockchain therefore a miner needs to
store the whole blockchain. This restricts the advantages of a node with large hash
power too. Furthur more the Wabei system specifically targets and limits an area
with more than 48% of the total hash power of the Wabei network. When an area’s
hash power exceeds 48% of the total network’s hash power the Wabei system will
block entry of new nodes in that area to limit the growth of its hash power.
3.4 Wabei’s Security Engine
1. The system picks a seed block and the distance between the latest block in the
blockchain and this seed block will be used to generate a hash value for later
calculations.
2. The seed block will be used to generate a 16MB pseudo-random cache.
3. This pseudo-random cache will be used to generate a 2GB dataset. A Wabei node
needs to store this dataset. And this dataset grows linearly as the blockchain grows.
The mining algorithm takes a specific part of the dataset and hash it to a hash
value. This specific part of the dataset can be generated from the pseudo-random
cache. This gives chances to a machine with low RAM to verify and mine a block.
The dataset is regenerated every thirty thousand blocks. A miner’s work is to read
through this dataset instead of performing heavy calculations which an ASIC rig can
do with much higher efficiency. Thus with this algorithm a common computer can
compete with an ASIC rig and has fair chances to mine a block successfully.
4. The mining algorithm in the Wabei system limits an ASIC chip to share RAM thus
restricting its mining advantages。  
![image3.1](./images/3-1.jpg "图3-1 比特币算力分布图")
<div align=center>图3-1 比特币算力分布图</div>

### 2.4 wabash Security Engine
 
1. The system picks a seed block and the distance between the latest block in the
blockchain and this seed block will be used to generate a hash value for later
calculations.
2. The seed block will be used to generate a 16MB pseudo-random cache.
3. This pseudo-random cache will be used to generate a 2GB dataset. A Wabei node
needs to store this dataset. And this dataset grows linearly as the blockchain grows.
The mining algorithm takes a specific part of the dataset and hash it to a hash
value. This specific part of the dataset can be generated from the pseudo-random
cache. This gives chances to a machine with low RAM to verify and mine a block.The 
dataset is regenerated every thirty thousand blocks. A miner’s work is to read
through this dataset instead of performing heavy calculations which an ASIC rig can
do with much higher efficiency. Thus with this algorithm a common computer can
compete with an ASIC rig and has fair chances to mine a block successfully.
4. The mining algorithm in the Wabei system limits an ASIC chip to share RAM thus
restricting its mining advantages.

   
## 三、钱包  
  
The Double block chain system has a decentralized wallet, Token-S. When a wallet is created its
private key and seed phrase are stored locally. If a user sends a transaction he will
sign the transaction off-line. The whole process is decentralized. It minimizes
chances of being attacked. Besides these the Token-S has the following features.  
![image4.1](./images/4-1.jpg "图4-1 token-S light wallet")
<div align=center>图4-1 token-S轻钱包</div>
  
### 3.1 Smart Security Check  
  
When a user logs into his Token-S wallet for the first time its smart security check
mechanism will be launched to check if this login device has potential risks and
alarm if it has. The login password is required to have at least six digits being
numbers and letters. This password is used to restore the wallet’s seed phrase and
sign a transaction. This password is stored locally in the user’s login device
insteadhttps://www.baidu.com/ of any other device. Token-S doesn’t provide amechanism 
to restore a password therefore a user must keep his password safe and secure.  
  
### 3.2 Multisig
  
In order to cope with hackers'stealing of private keys, a simple and effective way is 
to sign multiple signatures. In traditional Bitcoin accounts, each address in your Bitcoin 
address has a corresponding private key. Multiple signature addresses can have multiple 
associated private keys, and you need two of them to complete a transfer. In fact, 
you can also set it to 1/3, 5/5, 6/11, but the most common combination is 2/3, which 
is completed through Turing's complete contract layer. The contract uses sol language, 
which is highly extensible. Once the contract is deployed, no one can tamper with it. 
Assuming that every private key in an account managed by a double private key is 
acquired by a hacker, he can only transfer the amount within the daily limit. When
 the owner finds out, he can immediately terminate the loss. Happiness Public Chain 
is used for online wallet links in locks: htt://hwallet.bitwa.org. The use of online
 wallet needs to follow the instructions in https://github/wabei/hap-miner. The core 
operation is to unlock from the console in order to operate on the Web. The purpose
 of doing so is also to protect user privacy.
![image5.1](./images/5-1.jpg "图5-1 2/3模式的多重签名")
<div align=center>图5-1 2/3模式的多重签名</div>
In online wallets, more than two groups of private keys are stored independently in 
different locations. In order to ensure the security of wallets, the wallet UTC files 
are not allowed to be placed in the same location, otherwise the transfer is unsuccessful. 
In this way, even if any client node is broken, the funds are still safe. Online wallets 
are typically hot wallets, with the corresponding cold wallet mechanism, Token-s takes 
over the task.  
  
### 3.3 Cold Wallet  
  
Cold wallet means that the user completes the signature on other isolated network devices, 
and then completes the transaction by sending the signature through the hot wallet application 
scanning signature file. The private key is only stored in the cold wallet. This mechanism 
ensures that the private key never touches the network. General users need a non-networked 
terminal and install Token-s2.0 on it. After signing, they will directly generate two-dimensional
 code electronic pictures. Users can use token-S of another networked terminal device to scan the 
two-dimensional code of the signature of the off-line terminal to complete online transmission transactions.  
  
### 3.4 Secure and Trustworthy Trading Platform  
  
Token-S uses the world's top professional anti-fraud system to build a secure, compliant and high-credit
 trading platform. The digital assets of transactions can be traced, the sources and locations of assets 
can be checked to prevent fraud. Every transaction information can be queried through the transaction 
hash and browser: http://www.hapexplorer.com. At the same time, Token-S wallet will gradually ensure 
the security of users'digital assets. The functions of fingerprint, voice, pattern, venous unlocking 
and compound unlocking are added to ensure the safety and convenience of use.  
  
### 3.5 Anti-Quantum Encryption System  
  
For the sake of user's capital security, Token-S intends to restrict the way of miners'packing and checking surplus, so as to form a retrospective isolation mechanism. Firstly, when the miners need to check the surplus in packing, the miners can only know whether the transaction is in accordance with the rules (e.g. how much the balance of the account is compared with the upcoming expenditure), but they can not know the specific amount (to protect the privacy of users).

In addition, modern society is highly dependent on the Internet, people have to put some important private information and behavior habits on the Internet. The security risks brought by big data can not be ignored. If hackers get a lot of traces of user behavior, it may not take so long to crack a person's account. The advent of quantum computers has brought new challenges to the field of encryption. This is the case. At present, the known RSA encryption algorithm has been decoded by quantum computer. Double-chain uses Secp256K1 asymmetric encryption algorithm. Because of its technical characteristics, there is no way to solve it yet. In cryptography field, it is considered impossible for anyone to crack it in 15 years. It is extremely complex and arduous to do this thoroughly.
Secp256k1 refers to the parameters of ECDSA (Elliptic Curve Digital Signature Algorithms) curve used in Bitcoin, and is defined in Certicom Research (http://www.secg.org/sec2-v2.pdf).
    ![image3.5](./images/3-5.jpg "图3-5 椭圆曲线图")
    <div align=center>图3-5 椭圆曲线图</div>  
Secp256k1 is an elliptic curve based on Fp finite field. Because of its special construction, the performance of the optimized curve is 30% higher than that of other curves. It has two obvious advantages:
1) It occupies very little bandwidth and storage resources, and the length of the key is very short.
2) Let all users use the same operation to complete domain operations.
Elliptic Curve Digital Signature Algorithms (ECDSA)
User's key pair:
(D, Q)
Information to be signed: M
Signature:
Signature process:
1) Generate a key pair randomly according to ECC algorithm
2) Order
If r = 0, return to step 1
3) calculation
4) Convert H into a big endian integer e according to the data type conversion rule
5)
If s = 0, return to step 1
6) Output
That is signature.
Verification process:
1) calculation
2) Convert H into a big endian integer e according to the data type conversion rule
3) calculation
4) calculation
Verify that the signature is invalid if R = zero
5) Order
6) If v = r, the signature is valid, and if v_r, the signature is invalid.
0 x 01 Secp256k1 elliptic curve
The shape of Secp256k1 elliptic curve is as follows:
The parameters in elliptic curve domain are specified by element T = (p, a, b, G, n, h).
The figure above is an example of an elliptic curve, similar to the curve used in Bitcoin.
Bitcoin uses a special elliptic curve and a series of mathematical constants defined by the secp256k1 standard. The standard was established by the National Institute of Standards and Technology (NIST). The secp256k1 curve is defined by the following function, which can produce an elliptic curve:
Y2 = X3 + 7)} over (Fp)
or
Y2 mod p = X3 + 7 mod p
The above mod p (modulus of prime p) indicates that the curve is in the finite field of prime order p, and also writes Fp, where p = 2256-232-29-28-27-26-24-1, which is a very large prime.
Because this curve is defined in a finite field of prime order rather than in a real range, its function image looks like a scatter plot scattered on two dimensions, so it is difficult to draw a graph. However, the mathematical principle is similar to the elliptic curve in real number range. As an example, the following figure shows an elliptic curve in a finite field with a much smaller Prime Order 17 in the form of a series of scatters on the grid. Bitcoin elliptic curves of secp256k1 can be imagined as a series of more complex scatters on a large grid.
[image 3.6] (. / images / 3-6.jpg "Figure 3-6 Elliptic Curve Figure 2")
< div align = center > Fig. 3-6 elliptic curve Fig. 2 </div >
The figure is: elliptic curve on elliptic curve cryptography F (p). In the mathematical principle of elliptic curve, one point is called "infinite point", which roughly corresponds to the function of 0 in addition. In computers, it is sometimes expressed as X = Y = 0 (although it does not satisfy the elliptic curve equation, it can be tested as a special case). There is also a + operator, known as "addition", which is like the addition of real numbers in elementary mathematics. Given two points P1 and P2 on the elliptic curve, there must be a third point P3 = P1 + P2 on the elliptic curve.
In geometry, the third point P3 can be determined by drawing a line between P1 and P2. This straight line intersects exactly one point on the elliptic curve. This point is marked P3'= (x, y). Then, map on the x-axis to get P3= (x, -y). Here are a few special cases that can explain the need for the existence of infinity. If P1 and P2 are the same, the connection between P1 and P2 is the tangent of point P1. There is only one new point intersecting the tangent on the curve. The slope of the tangent can be calculated by differential method. The slope can be obtained even if the point of the curve is limited to two integer coordinates. In some cases (that is, if P1 and P2 have the same X value, but different Y values), the tangent will be completely vertical, in which case, P3 = the "infinite point". If P1 is "infinite point", then P1 + P2 = P2. Similarly, when P2 is infinite, P1 + P2 = P1. That's what makes infinity look like zero. It turns out that the + operator obeys the binding law here, which means (A + B) C = A (B + C). This means that we can write A + B + C without parentheses without confusion. We have defined elliptic addition, and we have a standard definition of multiplication for extended addition. Given the point P on the elliptic curve, if K is an integer, then kP = P + P + P +... + P (k times). Note that K is sometimes confused and referred to as an index. This is one of the most outstanding achievements in the field of classical cryptography at present, but is such an algorithm really absolutely safe? If we want to crack a private key, it will take 65 years for the world's top classical computer to crack, so hackers have no motivation to crack such a key system with the current technical conditions, because the cost of doing evil is much higher than the benefit. However, it is inappropriate to say that ECDSA is absolutely safe. A 10-bit quantum computer can easily crack RSA public-key encryption algorithm. ESDSA is essentially similar to RSA, and belongs to a complex cryptosystem. If a quantum computer reaches 100 qbit processing power, traversing curve coordinates, it will not take more than 15 minutes to complete the decipher by sign-in. In order to prevent future problems, we can't wait 15 years to develop corresponding anti-quantum cracking algorithms. We use the principles of quantum mechanics and the achievements of predecessors in the field of quantum encryption to start the system test of quantum encryption algorithm. Once the test is mature, we can switch the cryptosystem at any time when the community is consistent, so that even large-scale commercial quantum computers can be used. It's okay to come.
   
### 3.6 Exploration of Quantum Encryption
Quantum cryptosystem does not depend on mathematical complexity, but is guaranteed by the physical and natural characteristics of quantum uncertainty and non-reproducibility in physics. It has been proved that unconditional security can not be broken even by quantum computers. Quantum fingerprint signature algorithm is the basic signature algorithm in happiness chain quantum encryption test. The quantum fingerprint function used in quantum fingerprint signature algorithm is one of the quantum one-way functions. BB84 or BBM92 protocol is used for key distribution (which has high technical maturity). In this white paper, we introduce the quantum one-way function used in happiness public chain: the concept of classical one-way function is mapping f (i): I - > O. For any input i, I belongs to a specific set, and f (i) is easy to calculate, but it is very difficult to derive I by using f (i). I can be simply understood as the private key in block link, f (i) can be understood as the public key address; based on classical one-way function, I They can construct the quantum one-way function of happiness common chain, that is, the classical bit string K whose input length is L, and the quantum state | f (k) > of N qubits, where L > N, the mapping K - > F (k) > is easy to calculate, but it is impossible to find the inverse (as long as the sender does not voluntarily surrender his own K), because the qbit required for the inverse is only the upper limit of the number of classical bits, and the size of the state set of K may be 2 N times. At the same time, it satisfies Heisenberg's uncertainty and quantum non-replicability. Quantum unidirectional function is the cornerstone of various quantum cryptographic protocols. Quantum fingerprint (QFP) technology is also used in Happy Common Chain. Quantum fingerprint technology can compress the information of 120 classical bits to 70 quantum bits, which can greatly improve the security verification speed of Happy Common Chain. The user terminal and sending device and its preparation of quantum entanglement will become one of the public happiness chain project.

### 3.7 One-stop management of multi-chain wallet and currency  
Token-S decentralized wallets can be imported to create multiple wallets through mnemonics or private keys. Supporting Happiness Chain, Hanyuan Chain, Etaifang. Unified management of multiple wallets and currencies greatly reduces the threshold and management burden of digital currency, and effectively promotes the flexible application of digital assets.  
  
## 四、Ecological Construction of Public Chain
### 4.1 Application of public chain  
  
First of all, one of the two public chains, Hanyuan Chain has all the characteristics of the public chain, but it is built under the legal framework of China. It will not publicly issue tokens, and its digital currency will be used as a common integral purpose for technical incentives, transaction upload and consumption incentives. Happiness chain is built on the legal framework of Singapore, which will promote the global issuance of digital currency and its value concept.


In addition to providing more secure e-cash system services, Happiness Public Chain is also aimed at enabling developers to create arbitrary consensus-based, scalable, standardized, well-featured, easy-to-develop and collaborative applications. Public chains enable anyone to create contracts and de-centralized applications by establishing the ultimate abstract base layer - block chains with Turing's complete intelligent programming language built in - and set up freely defined ownership rules, transaction modes and state transition functions.


Keyword 1: STO


We hope that we can use block chain digital currency technology to construct a public value investment system which is independent by issuers and meets the market value investment concept and regulatory requirements. This value investment system is different from the traditional top-down company system and stock issuance system, but from the bottom-up consumer investment system. Its active right should belong to the consumer public, not monopoly capital. This coincides with the original intention of Bentong, who founded Bitcoin in the hope of exploring the establishment of a decentralized electronic cash system (self-trust system, There is no need for third-party credit enhancement, but 10 years later, the Federal Reserve or the Federal Reserve, Wall Street greed has increased, even in the digital money industry is rampant, relying on storytelling but not the actual application of ICO circle money cases everywhere. People's monetary autonomy is still unchanged. Obviously, it is not enough to issue de-centralized digital money, and it can not be supported by traditional value investors: STO, also known as asset digitization, will use physical objects to encrypt digital endorsement. Take WineC as an example, a WineC is equal to a wineC deposit produced in the period of 2019-2020 in the happy public chain. Wine, consumers can extract wineC red wine with WineC as withdrawal voucher at any time after purchasing WineC. WineC cash can also be sold in the capital market. Those who fail to take delivery can announce donation of auction proceeds or use auction proceeds to produce a new batch of equivalent liquor storage or direct reserve legal digital currency, which provides value support for WineC (the cost of storing legal digital currency is extremely low). The management cost of the period can be deducted from it. WineC's value fluctuation in the asset market conforms to the law of value investment and economic principles. Investors need to go deep into the depth of economics, excavate and judge the future supply and demand of products, and make short-term, medium-term and long-term investment and trading arrangements. If the idea and plan of Happy Public Chain can be implemented successfully, the future enterprises will not need to issue stock financing, only need to sell their own vouchers. Investors will construct expected return curves according to product competitiveness, future macro and micro supply and demand, team capacity and so on. Because toothpicks and ice cream have a short production cycle, demand and price will be negatively correlated, but environmental control and sugar import restrictions may lead to different changes in the short-term yield curve; while scarcer products will show a positive correlation between demand and price, unless there is a financial crisis and supply exceeds demand, the curve will reverse. For the fast consumables with saturated materials and easy to produce, the issuing company may have to offer the obligation of repurchase, or give a big discount on the basis of the current market price, or its R&D technology and sales control strategy can meet a unique market demand, so as to maintain the high price of the product in the investment cycle. It should be pointed out that the de-centralized e-cash system constructs an endorsement-free public trust mechanism, rather than removing the centralized public administrator, which is not the original intention of Zhongben Cong.


If technology, especially public chain technology, can't make people live better, this technology has no value. Fortunately, countless global technological elites and operators are making efforts to this end. If STO succeeds in the end, then enterprises can pre-sell currency voucher financing, inventory security financing, pre-sale intangible assets equity financing, competitive products may be pre-sold. When the capacity of the next three years is sold out on the day of sale, enterprises can get good financing support while providing services to the society, without resorting to monopoly capital exploitation; there is no difference between oligarchs and civilians, where oligarchs'capital can not be as big as cowhair's consumption capacity even with the help of leverage, just as sharks' size can not be as big as the sea.


Keyword 2: Intelligent Code Uplink:


With the development of artificial intelligence, all kinds of robots will fill people's lives. Hawking once predicted that artificial intelligence will destroy and recognize human beings. An automated hummingbird robot cluster can kill people in a city. This is not a night talk. While enjoying artificial intelligence as a substitute, we are also facing the threat of robotic technology. Robot code is chained, open and transparent, and can not be tampered with. It will facilitate users'safe use of robots and government safety supervision. In the future, the Happy Public Chain R&D team will continue to expand AI technology and share it with the society when it is mature, so as to enhance the use value of public chains and encourage global developers to upload intelligent codes. These codes need to pay a certain amount of token when they are reused. Developers can benefit from users'use because the code upload chain can not be tampered with.Publish a new call address, users can choose different versions and different on-line addresses for trial. All security-related technologies can be linked in this way, such as anti-virus software. You may wonder whether he is anti-virus or spoofing. Lottery lottery prize-opening algorithm can also be linked in this way to avoid misunderstanding and improve credibility.

Keyword 3: Other:

Future applications such as decentralized voting decision-making and community governance.

  
### 4.2 Distribution and use   
  
Double public chains contain two sets of independent parallel public chains, one set of public chains we call Happy Public Chains, the name of which is HAP, Chinese translation: Fubei, which is a fully open technology platform, including all its ecological applications; the other set of public chains we call Hanyuan Public Chain, precisely combines its ecological application scenarios, we can understand the former as the "number of assets" of the block chain system. The latter is the "public traceability platform" in the block chain system. Its name is HSC, Chinese translation: Chinese source integral, HAP coin and HSC integral play dual roles, providing the main liquidity for various digital asset transactions, and more importantly, providing a mechanism to pay transaction costs.
The total number of happiness chains is 100 million, which is released by lock warehouse every day. The total amount of miners'annual mining is about 5 million, which is equivalent to 5% of the total amount. It is one third of Taifang's circulation, that is, to supplement the loss caused by key loss, password forgetting, mobile phone loss and theft every year.
The circulation of Hanyuan Chain is 50 billion, and the technical maintenance incentive of public nodes is about 50,000 per year. After deduction of loss, the overall number of deflation is controlled below 50 billion. Hanyuan Chain is not listed on the market, and is only used as a common digital traceability integral.
The distribution model is as follows:
Through the sales activities, the happiness chain will be sold at 0.15 yuan per unit. Early purchasers will enjoy larger discounts, and the proceeds of the sale of digital currencies such as BTC/ETH will be used entirely to pay the wages and rewards of developers and researchers, as well as to invest in cryptographic monetary ecosystem projects.
One-third of Bay will be allocated to early contributors to development before BTC/ETH or other deterministic financing succeeds, another one-third will be allocated to long-term research projects, and one-third to city maintenance. Hanyuan points are not considered for listing.
  
### 4.3 Conclusion: A safer decentralized e-cash system
 
The use of the above security mechanism makes it more advantageous than traditional digital currency in terms of centralized calculation and transaction security. It reduces the benefits of large mines and makes joint mining unnecessary, because it does not significantly improve the benefits of miners; on the other hand, it provides more secure wallet applications, multiple signatures, anti-malicious traceability mechanism, and the use of artificial intelligence, so that even careless users can effectively defend against hacker attacks. In particular, the Hanyuan chain is expected to become the first public block chain traceability system in China, and incorporates the security characteristics of the dual public chain.
  
## 关于我们  
汉源公链（中国），由中国内蒙古汉森集团运营
源码地址：https://github.com/wabei/go-hsc  
在线钱包：http://wallet.bitwa.org(与挖矿客户端配套使用）
浏览器地址：www.hscexplorer.com
官网地址：www.bitwa.org  
联系邮箱：service@bitwa.org  

幸福公链（新加坡），由新加坡海丝基金会运营管理
源码地址：https://github.com/wabei/go-hap
浏览器地址：www.hapexplorer.com
在线钱包：http://hwallet.bitwa.org(与挖矿客户端配套使用）
官网地址：www.liananhjb.org  
联系邮箱：hap@bitwa.org


 




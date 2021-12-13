# Permission Blockchain Network based Central Bank Digital Currency
## Abstract
The central bank digital currency (CBDC) is gaining popularity for the last few years in many countries as it will affect the entire ecosystem of the current financial infrastructure. The CBDC utilizes digital tokens to indicate any nation’s fiat/stable currency that manages under distributed ledger technology such as blockchain. Compared to existing cryptocurrencies, the CBDC is regulated by the government monetary policies, including the issuance of digital tokens (i.e., digitized central bank money) and circulation of these digital tokens to the commercial banks, then to the public/end-users. This paper proposes a two-layered CBDC architecture after analyzing the recent research and existing CBDC pilot projects. The distribution layer shows wholesale CBDC based on permission blockchain network (PBN) between the central bank and the commercial banks. While, the user layer describes the functioning of retail CBDC, which shows the interaction between the commercial banks and the end-users through the token-based account. We aim to provide the CBDC design architecture and smart-contract functions for PBN.
## I. INTRODUCTION
The popularity of cryptocurrencies such as Bitcoin [1], Ethereum [2], XRP [3], etc., is gaining attention and speeding up their circulation worldwide. These cryptocurrencies are not regulated by any centralized authority (i.e., government) also not considered as legal tender, which could lead to the support for anti-money laundering (AML), financing of terrorism (CFT), and other criminal activities. In particular, several countries are afraid of these illegal cryptocurrency circulations and planning to implement their legal digital money called central bank digital currency (CBDC). The CBDC uses digital tokens generated by converting any nation’s fiat/stable currency into digital tokens using distributed ledger technology (DLT) [4]. Unlike other cryptocurrencies, these digital tokens are generated by the nation’s monetary authority and issued and regulated under the central bank’s governance. Therefore, these digital tokens are pegged by a suitable amount of monetary assets such as gold or foreign currency reserves. The adoption of DLT in CBDC improves the current financial infrastructure by building trust in the issuance and circulation of digital tokens. The DLT enhances CBDC through fast and efficient processing of digital tokens, introduces transparency for validation of digital tokens, and makes overall CBDC architecture safer and inexpensive. The DLT records all the transactions in its immutable ledger, ensuring integrity, trust, and robustness in the CBDC network [5]. The bringing of CBDC in any nation may address current financial infrastructure vulnerabilities and inefficiencies by introducing decentralized monetary policies, a distributed secure payment system, reducing counterparty risks, stabilizing the financial payment market, etc.
There exist two types of CBDCs such as wholesale CBDC and retail CBDC. The wholesale CBDC is for the authorized financial institutions that carry reserve deposits with the central bank [6]. A wholesale CBDC is issued, distributed, managed, and stored entirely by the central bank or by an authorized institution appointed by the central bank to perform such tasks. The entities involved in the wholesale CBDC are not anonymous because they pre-register themselves under the central bank to access and conduct interbank payment settlement transactions processed by the central bank or through the authorized institution. The benefit of bringing wholesale CBDC in place of the traditional wholesale market is enhancing security and payment settlement efficiency, enabling real-time monitoring, minimizing counterparty credits and liquidity risk. On the other side, the retail CBDC is issued for the general public to purchase goods and services and send/receive digital tokens for fulfilling their routine demands [7]. The idea of retail CBDC is to promote a cashless society to reduce cash printing costs and make payments outside of the banking system, similar to cash payment [8].
In CBDC, the end-users can access the digital tokens using an account-based CBDC or token-based CBDC [9], [10]. In account-based CBDC, the end-user opens an account with the third-party provider authorized by the central bank. Hence, the third-party provider is responsible for end-user identity verification, know-your-customer (KYC) process, digital tokens distribution from one account to another, and transaction’s approval, e.g., commercial bank accounts. In token-based CBDC, an end-user requires a digital wallet to hold digital tokens accessed by a public/private key pair or digital signature. Therefore, the third-party provider approved the transaction based on the public/private key of the end-user. Also, a token-based CBDC may incorporate end-users identity to remove anonymity from the CBDC network, e.g., cash and crypto coins (i.e., bitcoin, ether, etc.).
At present, several countries are focusing on the research and development of CBDC. The People Bank of China was the first central bank and started researching CBDC in 2014, which later established a digital currency research institute in 2017 [11], [12]. The Bank of China’s CBDC project is called DC/EP (digital currency electronic payment), which addresses the wholesale and retail sector by developing digital Yuan. The Bank of England initiated its research into the CBDC project called RSCoin in 2015, which focuses on retail payments [13]. The Bank of Canada has actively researched CBDC since 2016 and proposed a CBDC project called Jasper, which aims to explore the possibility of creating a payment system for wholesale by issuing the Canadian digital dollar named CADCoin [14]. The Bank of Bahamas released its public document on CBDC in 2017 with the CBDC project name Sand Dollar and selected exuma island to experiment with the digital Bahamian dollar in the retail and wholesale domain [15].
Similarly, the countries collaborate on joint CBDC projects such as project Stella, Ubin, LionRock, etc., [16] to explore cross-border payments opportunities. So far, the Reserve Bank of India (RBI) has also started investigating CBDC opportunities and challenges in India and published a report on currency and finance 2020-21 [17]. RBI focuses on CBDC design’s benefit by promoting non-anonymity at the end-user level, monitoring financial transactions, pumping the central bank helicopter money, and supporting financial inclusion by direct transfer to increase social welfare. On the downside, the central bank pegged digital money may pose a possibility of disintermediation of the banking system. The RBI mentions a possible solution to overcome this problem by establishing a two-tier remuneration system for CBDC, lacking a design description.
In this paper, we propose a CBDC model using blockchain technology. We did a thorough study on the existing CBDC projects and introduced a two-layered model, explaining wholesale and retail CBDC. Further, we take an interbank settlement example to illustrate the back-end functionality for domestic payments and transfers using our proposed system model.  The rest of the paper is organized as follows. The related work is discussed in section II. CBDC overview and related technology are briefly outlined in Section III. In section IV, the proposed CBDC architecture is presented. Finally, concluding remarks and future work is given in Section V.
## RELATED WORK ##
In the paper [18], the author proposes a two-tier CBDC model for distributing digital currency in a wholesale DLT network. This digital currency is widely available for the general public using accounts provided by commercial banks. The disadvantage is that the author’s concept is valid for the small pilot project not acceptable at the country level. In the paper [19], the author designs a CBDC model using the permission blockchain called MBDC. For improving the scalability and payment process, the multi-blockchain architecture and Chain ID are utilized in the MBDC to distinguish between commercial banks and their sub-branches with the drawback of processing overhead due to the multi-blockchain layer. In the paper [20], the author proposes a CBDC model named Panda based on the dual blockchain system to maintain transaction data and account history separately with an efficient consensus protocol (i.e., BFT). They are also ensuring that only authorized parties have access to view the blockchain data. Perhaps running more than two blockchains simultaneously on the same network could lead to scalability problems and require high maintenance. In the paper [21], the author proposed a three-layer blockchain-based framework for CBDC to describe the entire lifecycle of CBDC from issuance to withdrawal of digital currency with an example of cross-border payment to describe the transaction payment and settlement through CBDC. In the paper [22], the author proposed the working of retail CBDC using token-based CBDC without DLT and focuses on many aspects such as digital signatures, blind signatures, key-exchange protocol to protect against AML/ CFL attacks and to bring anonymity during the transaction. Overall, most of the authors fulfill their work objectives in their terms and conditions, with a lack of issues. In this context, we present a two-layered CBDC framework after analyzing the existing research work. 
## II. BACKGROUND ##
### A.) CBDC Architecture ###
The CBDC architecture follows one of the available two implementation approaches: direct CBDC and indirect CBDC. 
### a.)	Direct CBDC
In direct CBDC design, the central bank operates the digital tokens payment system and offers retail services to the end-users. Therefore, it is also called single-layered architecture. Any end-user can open an account in the central bank to receive digital tokens, as illustrated in Fig. 1. The central bank itself maintains the ledger of all accounts and executes retail payments. Therefore, it has complete control over the issuance and circulation of digital tokens. On the other side, the disadvantage of having this model is the tremendous workload. The central bank needs to provide good services to individuals and implement government regulations to prevent AML and anti-fraud prevention on all accounts.
![Fig 1: Direct CBDC](Images/directCBDC.jpg) 
```
Figure 1: Direct Central Bank Digital Currency
```
### b.)	Indirect CBDC
In the indirect CBDC model, the central bank creates and holds digital tokens. Still, intermediaries include commercial banks, are in charge of distributing these digital tokens, managing accounts and retail services for the end-users, as represented in Fig. 2. This model is similar to the current payment system and is sometimes known as the two-layered/intermediary model. The main difference is commercial banks request digital tokens from the central bank instead of end-users. This central bank manages the commercial bank’s account in its ledger to identify the digital tokens in circulation. The advantage of having this model is that it reduces the central bank load, encourages intermediaries to improve services for their customers, easy tracking of AML, fraudulent activities, etc.
![Fig 2: Indirect CBDC](Images/IndirectCBDC.jpg) 
```
Figure 2: Indirect Central Bank Digital Currency
```
### B.)	Distributed Ledger Technology (DLT) ###
Over the last few years, the financial sector has started exploring the DLT or blockchain to overcome existing financial sector challenges by leveraging greater transparency and improving the efficiency of clearing and settlement. The blockchain is an immutable database that continuously grows, replicates, and synchronizes among the blockchain nodes. Therefore, the blockchain nodes are responsible for achieving consensus over the shared transactions in the blockchain network, whether to add or reject the proposed transactions. There exist multiple consensus protocols such as proof of work, proof of stake, delegated proof of stake, practical byzantine fault tolerant, etc., [23] supported by either public or private blockchain. The public blockchain is open to everyone participating in the blockchain network, which is generally open-source and leveraged by the community. e.g., Bitcoin and Ethereum blockchain platforms. In comparison, the private blockchain is established, control and access only by the trusted or known entities. e.g., Hyperledger Fabric blockchain platform [24]. Any blockchain, either public or private, contains four core parts to enable blockchain functionalities. These are (a) block, (b) chain, (c) network, and (d) smart contract. The block is a collection of transactions with a time-stamp where the transaction contains any activity data such as money transfer between payer and payee. The chain represents the links between the new and previous blocks by interconnecting each other through a hashing algorithm. The blockchain’s network contains blockchain nodes that keep the entire record of all valid blocks. However, the smart contract is a program that indicates the multiple functions of any blockchain application stored on the blockchain network. This smart contract executes automatically by triggering an event on the blockchain network.
### C.)	Facebook Diem Project ###
Facebook started investigating CBDC with facebook libra project, later updated as the diem project. Since then, different countries start exploring this project to search for the possible opportunities of CBDC in their nation and came up with their revolutionary ideas and CBDC design to endure the existing financial sector. The libra association published its whitepaper [25], enabling a simple global payment system and financial infrastructure that empowers billions of end-users. The libra global payment system utilizes the libra blockchain, an open-source blockchain, and builds from scratch to target scalability, security, storage, and throughput issues. The libra blockchain started with libra byzantine fault tolerance (LibraBFT) protocol for achieving consensus, subsequently updated as DiemBFT. Later, facebook improved its existing libra project called libra 2.0, in which the diem association proposed change in four areas. First, instead of focusing on a single type of libra coin, libra plans to add several digital stable coins available in the libra network. Second, libra introduced enhance compliance procedures to protect against AML and to finance illicit activity. Third, pegged libra stable coins with a sovereign currency, and finally, the libra network transition from permissionless to permission.
## IV.	PROPOSED FRAMEWORK FOR CBDC ##
In this section, we present a two-layered CBDC framework considering the current financial infrastructure. The upper layer describes the wholesale CBDC through the distribution layer, whereas the lower layer specifies the retail CBDC using the user layer. Here, we focus on the design and working of CBDC, which is briefly described.
## A.) Distributed Layer ##
The distribution layer is a collection of the central bank, denoted by RBI and commercial banks indicated by, {〖CB〗_i } where i∈{1,…,n} as shown in Fig. 3. The central bank creates a permission blockchain network (PBN) which contains a central bank, commercial banks, and a certificate authority (CA). This PBN can be generated using existing blockchain frameworks such as Hyperledger Fabric, R3 Corda, etc., or the central bank may create its own customized PBN platform. Perhaps, the central bank remains the in-charge of publishing various smart contracts, including registration of central bank, digital certificate generation, tokens generation, registration of commercial bank, request for tokens, and interbank settlement in PBN at the distribution layer indicated in Fig. 4. The CA is the legitimate blockchain node, represented by 〖{BC〗_CA}. Further, it is responsible for issuing digital certificates (i.e., follow X.509 internet standards) to the central bank and the commercial banks in the PBN. This digital certificate binds the bank’s original identity (either central or commercial) and authenticates it while sending sign transactions in the PBN.
**(i).** ***Wholesale CBDC :***
The wholesale CBDC is for the authorized financial institutions that carry reserve deposits with the central bank. A wholesale CBDC is issued, distributed, managed, and stored entirely by the central bank or by an authorized institution appointed by the central bank to perform such tasks. The entities involved in the wholesale CBDC are not *anonymous* because they pre-register themselves under the central bank to access and conduct *interbank payment settlement* transactions processed by the central bank or through the authorized institution. The benefit of bringing wholesale CBDC in place of the traditional wholesale market is enhancing *security* and *payment settlement efficiency*, *enabling real-time monitoring*, *minimizing counterparty credits* and *liquidity risk*.  
**(ii).** ***Retail CBDC :*** 
On the other side, the retail CBDC is issued for the general *public* to purchase goods and services and send/receive digital tokens for fulfilling their routine demands. The idea of retail CBDC is to promote a *cashless society* to reduce cash printing costs and make payments outside of the banking system, similar to cash payment.
### B.) Account-based and Token-based CBDC
In CBDC, the end-users can access the digital tokens using an account-based CBDC or token-based CBDC.     
**(i).** ***Account-based CBDC :*** 
In account-based CBDC, the end-user opens an account with the third-party provider authorized by the central bank. Hence, the third-party provider is responsible for end-user *identity verification*, *know-your-customer (KYC)* process, *digital tokens distribution* from one account to another, and transaction’s approval, e.g., *commercial bank accounts*.   
**(ii).** ***Token-based CBDC :*** 
In token-based CBDC, an end-user requires a *digital wallet* to hold digital tokens accessed by a public/private key pair or digital signature. Therefore, the third-party provider approved the transaction based on the public/private key of the end-user. Also, a token-based CBDC may incorporate end-users identity to remove anonymity from the CBDC network, e.g., *cash* and *crypto coins* (i.e., bitcoin, ether, etc.).
## CBDC Architecture
The CBDC architecture follows one of the available two implementation approaches: direct CBDC and indirect CBDC.  
**(i)** ***Direct CBDC :***
In direct CBDC design, the *central bank* operates the digital tokens payment system and offers retail services to the end-users. Therefore, it is also called *single-layered architecture*. Any end-user can open an account in the central bank to receive digital tokens, as illustrated in Figure. 1. The central bank itself maintains the ledger of all accounts and executes retail payments. Therefore, it has complete control over the issuance and circulation of digital tokens. On the other side, the **disadvantage** of having this model is the tremendous *workload*. The central bank needs to provide good services to individuals and implement government regulations to prevent AML and anti-fraud prevention on all accounts.

![Fig 1: Direct CBDC](Images/directCBDC.jpg) 
```
Figure 1: Direct Central Bank Digital Currency
```
**(ii)** ***Indirect CBDC :*** 
In the indirect CBDC model, the central bank creates and holds digital tokens. Still, intermediaries include commercial banks, are in charge of distributing these digital tokens, managing accounts and retail services for the end-users, as represented in Figure. 2. This model is similar to the current payment system and is sometimes known as the *two-layered/intermediary model*. The main difference is commercial banks request digital tokens from the central bank instead of end-users. This central bank manages the commercial bank’s account in its ledger to identify the digital tokens in circulation. The **advantage** of having this model is that it reduces the central bank load, encourages intermediaries to improve services for their customers, easy tracking of AML, fraudulent activities, etc.
![Fig 2: Indirect CBDC](Images/IndirectCBDC.jpg) 
```
Figure 2: Indirect Central Bank Digital Currency
```

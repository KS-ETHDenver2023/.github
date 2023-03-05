

# **Litepaper: Alice’s Ring**
  
  
## **Plan :**

1.  Executive Summary
    
2.  The problem

3.  The solution
    
4.  How it works
    
5.  Use Cases

6.  Compliance
    
7.  Market Analysis
 
8.  Marketing strategy
    
9.  Product development
    
10.  Sales Strategies
    
11.  Team
 
12.  Technical roadmap
 
 
****
Privacy is at the core of the blockchain ecosystem and at the center of the original ideals of the Cypherpunks. However, today with the growing number of blockchain applications in our ecosystem with use cases increasingly connected to the rest of the world (apartment rental, tokenization of real-world assets, DID...), it is becoming increasingly difficult to detach one's on-chain identity from one's own identity.

  

## **1.  Executive Summary**
    
Alice's Ring is a solution that addresses the growing need for privacy in the blockchain ecosystem by providing a means for individuals to prove solvency without revealing their wallet address or transaction history. This is achieved through the use of cryptographic ring signature technology and other cryptographic means to generate verifiable, solvency proofs at a specific point in time. The solution is designed for individuals who value their privacy while transacting on blockchain platforms, and it offers a unique value proposition by allowing users to prove solvency without compromising their privacy.

  

## **2.  The problem**
    
The Ethereum Virtual Machine (EVM) is a fundamental component of the Ethereum network, allowing developers to create and execute smart contracts. While the EVM provides a powerful tool for building decentralized applications and executing code on the Ethereum blockchain, there are currently no EVM-based solutions specifically designed for generating solvency proofs. This gap in the market creates an opportunity for solutions like Alice's Ring to offer a new, innovative approach to generating proof of solvency that provides greater privacy and security for users. By leveraging cryptographic ring signatures and other cryptographic means, Alice's Ring can generate verifiable solvency proofs that do not reveal the user's on-chain assets and history associated with their own identity, filling a need that is currently unmet by EVM-based solutions.

SECP256k1 is a widely used elliptic curve cryptography algorithm that is used in many blockchain applications, including Bitcoin and Ethereum. While SECP256K1 provides a secure means of generating cryptographic signatures and keys, it is not ideally suited for use in zero-knowledge proofs (ZKPs) such as ZK-SNARKs.

ZK-SNARKs require pairing-friendly elliptic curve cryptography, which is not a property of SECP256K1. This means that implementing ZK-SNARKs with SECP256K1 is not straightforward and requires additional workarounds that can significantly reduce the efficiency and security of the system.


As Alice's Ring is designed to provide a highly secure and efficient means of generating verifiable solvency proofs, the team behind the project needs to carefully consider the cryptography algorithms used in the solution. While SECP256K1 is a widely used and secure algorithm, it is not ideally suited for ZK-SNARKs, and other cryptography algorithms may need to be considered to ensure the best possible security and efficiency for the solution.

## **3.  The solution**  

Our solution stands in 2 words : Ring Signatures. Ring signatures are a type of digital signature that allows a member of a group to sign a message on behalf of the group without revealing which member actually signed the message. In other words, a ring signature makes it impossible to determine who exactly in the group signed the message, while still proving that someone in the group did sign it.

The name "ring signature" comes from the way the signature is created. It involves a "ring" of public keys belonging to group members, and the signature is formed by combining the signer's private key with the public keys of other members in the ring. The result is a signature that can be verified by anyone using the group's public keys, but cannot be traced back to the individual who actually signed it.

Ring signatures have a variety of applications, including enhancing privacy in blockchain transactions. They are often used in privacy-focused cryptocurrencies like Monero to obscure the sender's identity and make transactions unlinkable.

Ring signatures are considered to be EVM (Ethereum Virtual Machine) friendly because they are based on elliptic curve cryptography, which is the same cryptography used by Ethereum. In addition, ring signatures do not require any special hardware or software to run, as they can be implemented using smart contracts on the Ethereum blockchain.

Moreover, ring signatures are a proven and well-established cryptographic technique that has been widely used in the cryptocurrency industry, particularly for privacy-focused applications. The underlying math is well-understood, and implementations of ring signatures have been tested and reviewed by the cryptography community, providing a high level of confidence in their security.

Ring signatures are also highly efficient, allowing for fast and scalable computation of cryptographic signatures, which is important in the context of blockchain applications where speed and scalability are critical. As a result, ring signatures are a good choice for applications that require fast and secure cryptographic operations, such as Alice's Ring's solvency proof generation.

Overall, the use of ring signatures in Alice's Ring makes it an efficient and secure solution for generating verifiable solvency proofs on the Ethereum blockchain.

Ring signatures are considered scalable because they can be verified quickly and efficiently, even when the size of the signing group is very large. This is because the verification process only involves checking a single signature, rather than verifying multiple signatures from each member of the group.

When a signature is generated using a ring signature scheme, it includes information about the entire group of public keys, but does not reveal which specific key was used to create the signature. This means that anyone can verify the signature by checking that it was produced using one of the public keys in the group, without having to perform additional computations to verify each individual key in the group.

This makes ring signatures particularly useful in applications that require fast and efficient signature verification, such as in the context of blockchain transactions, where multiple signatures may need to be verified in a short period of time. Additionally, the fact that ring signatures are scalable makes them well-suited to use in decentralized systems, where a large number of participants may need to sign and verify messages on a regular basis.

  
## **4.  How it works**  

**Step 1 :** Generating the solvency proof

![](https://lh6.googleusercontent.com/_dzooHhCpndQ4iCjC95nKI41aj-tZLbtBkaXQ8Q32uM4aYvVNw4pg9zQ2zdvaWjvNOoUAa7KgzTFcJVK_yOtw6v6dxNjpMpwGnzKJCOmpey6giR53IDc7pDGOH_ro290HGssEyi_KVyXG41JXPe13KA)

Alice wants to generate a solvency proof for Bob :

1.  Alice visits our website
    
2.  She follows the easy steps
    
3.  She uses her wallet (Metamask, Coinbase wallet or WalletConnect) to send the proof to the on-chain verifier
    
4.  If her proof is valid, Alice will receive a SoulBound Token on her communication address as a proof of her solvability
    
5.  The SoulBoundToken can now be shown to anyone
  

**Step 2 :** Agreement

![](https://lh3.googleusercontent.com/hiCF517BlU-vz-x1TLLvdIAQRkGX_Mojwv5e9eRMGatGlrNOz27U61-seWmNmV6kAlRBkoLkBMkkxO3fh5i_8fOeNZGLR8ytozUsIX-v_oljPGb3cNQ-AvoyizLHMWzzjsakYQm4aBj9cRBXBptVNMY)

Bob want to verify Alice’s proof :

1.  Bob goes to Alice’s Ring Dapp, in the check proof section
    
2.  He fills in Alice's communication address as well as the ID of the SoulBound token given by Alice
    
3.  If a corresponding SoulBound token owned by Alice exists, it will be displayed
    
4.  Bob verify all the infos that he need to know


**Step 3 :** Transfering the funds

![](https://lh5.googleusercontent.com/94GTAhV4-xqVLD5kvVYSXtGT3AEeCLzV64mlZ4UNHXlVKW76lEfJzxV8v56HpnnnTEAg4QXbkpwzh4IvOZtWDQahbkyJLrBCJYkL_-81Pka6vXceidBT-V9rFOsusbnTB7pBfi1w3PKs8LvnTcp3qdA)

Now that Alice's proof of solvency has been verified by Bob, it's time for payment. In order not to reveal her address, Alice uses ZkBob :

1.  Alice goes to our website
    
2.  She connects her wallet and follows the steps
    
3.  She signs the transaction
 
## **5.  Use Cases**
    

Solvency proofs open possibilities for many things, particularly those involving financial transactions on the blockchain. Here are some examples of use cases for solvency proofs:

**Renting:** As described in the original MVP, solvency proofs can be used in the context of renting apartments or other properties. Landlords can require proof of solvency from tenants to ensure that they have the financial means to pay rent for a certain period of time. Solvency proofs can be generated without revealing the tenant's wallet address or transaction history, protecting their privacy.

**Loans:** Solvency proofs can also be used in the context of loans, where lenders may require proof of the borrower's solvency before extending credit. By providing a solvency proof, borrowers can demonstrate their financial status without revealing their wallet address or transaction history to the lender.

**Investments:** Solvency proofs can be used in the context of investments, where investors may require proof of a company's or individual's solvency before investing in them. By providing a solvency proof, the company or individual can demonstrate their financial status without revealing their wallet address or transaction history to the investor.

**Insurance:** Solvency proofs can also be used in the context of insurance, where insurers may require proof of the policyholder's solvency before issuing a policy. By providing a solvency proof, the policyholder can demonstrate their financial status without revealing their wallet address or transaction history to the insurer.

**Procurement:** Solvency proofs can be used in the context of procurement, where government agencies or private companies may require proof of solvency from contractors before awarding contracts. By providing a solvency proof, contractors can demonstrate their financial status without revealing their wallet address or transaction history to the agency or company.

**Real estate transactions:** Solvency proofs can be used in the context of real estate transactions, where buyers or sellers may require proof of solvency before entering into a contract. By providing a solvency proof, the buyer or seller can demonstrate their financial status without revealing their wallet address or transaction history.

**Gaming:** Solvency proofs can be used in the context of gaming and online gambling, where players may need to demonstrate their solvency in order to participate in certain games or tournaments. By providing a solvency proof, players can demonstrate that they have sufficient funds to participate without revealing their wallet address or transaction history.

**Charitable donations:** Solvency proofs can be used in the context of charitable donations, where donors may want to ensure that their contributions are going to a financially stable organization. By providing a solvency proof, the organization can demonstrate its financial status without revealing its wallet address or transaction history.

**Crowdfunding:** Solvency proofs can be used in the context of crowdfunding campaigns, where organizers may need to demonstrate their solvency to potential backers. By providing a solvency proof, the organizer can demonstrate that they have the financial means to carry out the project without revealing their wallet address or transaction history.

**Supply chain financing:** Solvency proofs can be used in the context of supply chain financing, where suppliers may need to demonstrate their solvency in order to secure financing. By providing a solvency proof, the supplier can demonstrate its financial status without revealing its wallet address or transaction history to the financing party.

These are just a few examples of the many potential use cases for solvency proofs. Any situation where a party needs to demonstrate their financial status without revealing their wallet address or transaction history on the blockchain could benefit from the use of solvency proofs.  

## **6. Compliance**

Compliance with institutional requirements is of paramount importance to Alice's Ring. We offer a service that remains 100% compatible with the laws put in place by the different states since our modules do not allow money laundering in any way. In addition, the ZkBob tool that we are implementing puts in place limitations on the use of its protocol and may have to request a KYC to fight against the laundering of stolen money.

## **7.  Market Analysis**

### **Potential customers :**

The potential customers for Alice's Ring solution could include:


**Individuals:** Individuals who are concerned about privacy on the blockchain could be potential customers for Alice's Ring solution. These individuals could be cryptocurrency users who want to protect their transaction data from being traced or linked to their real-world identity.

  

**Businesses:** Businesses that use blockchain technology for various purposes, such as supply chain management, payment processing, and data storage, could also be potential customers for Alice's Ring solution. These businesses may want to protect their transaction history and main wallet info from competitors, hackers, or other third parties.

**Financial Institutions:** Financial institutions that deal with cryptocurrency transactions, such as exchanges and wallets, could also be potential customers for Alice's Ring solution. These institutions may want to enhance the privacy and security of their customers' transactions to protect them from fraudulent activities. During a financial check, for example, the platform will be able to prove that such a user does indeed hold a certain amount of tokens without having to leak his address.

**Non-profit Organizations:** Non-profit organizations that rely on donations or fundraising through cryptocurrency transactions could also be potential customers for Alice's Ring solution. These organizations may want to protect their donors' transaction data and maintain their privacy and pseudonym on the blockchain.

### **Competitors :**

While Alice's Ring is a unique solution that offers a specific set of features and benefits, there are a few potential competitors that offer similar solutions for privacy-enhanced transactions on the blockchain:
 
**Mixers:* Mixers are a popular solution for enhancing privacy on the blockchain by obfuscating the transaction history. There are several mixers available in the market, such as Wasabi Wallet or CoinJoin applications.

**Private Chains:** Private blockchain networks offer enhanced privacy by restricting access to the network and the transaction data. Solutions like Corda and Hyperledger Fabric are examples of private blockchain networks that offer enhanced privacy and confidentiality.

**Mimblewimble-based Blockchains:** Mimblewimble is a protocol that offers enhanced privacy by obfuscating transaction data. Blockchains like Grin and Beam are examples of Mimblewimble-based blockchains that offer enhanced privacy for transactions.

**TumbleBit:** TumbleBit is a solution that offers privacy-enhanced transactions by using a combination of cryptographic techniques like coin shuffling, encryption, and hashing. It is currently available as an extension for the Bitcoin Core wallet.

**Privacy based blockchains:** Zero-knowledge proof blockchains like Zcash, Monero, Horizen, and others use cryptographic techniques to ensure the privacy and confidentiality of transactions on the network. These blockchains offer enhanced privacy for transactions, similar to Alice's Ring.
 

**Market trends :**

As privacy become increasingly important in the blockchain ecosystem, there is a growing demand for solutions like Alice's Ring that offer enhanced privacy for transactions. The market trend for privacy-enhanced blockchain solutions has been on the rise in recent years, with a particular focus on the Ethereum ecosystem. Many new privacy-focused projects have emerged, offering unique features and benefits to users.

The trend towards privacy on the blockchain is being driven by several factors, including concerns about surveillance, data breaches, and identity theft. As the number of blockchain applications and use cases expands beyond the traditional cryptocurrency sphere, the need for privacy is becoming more acute.

As a result, we can expect to see continued growth in the market for privacy-enhanced blockchain solutions like "Alice's Ring," as more individuals and businesses seek to protect their transaction data and maintain their privacy on the blockchain. However, there may also be challenges in this market, such as regulatory issues and concerns about the use of privacy-enhanced technologies for illicit purposes.
  

## **8.  Marketing strategy**

**Target Audience:** As previously mentioned, our target audience includes individuals, businesses, financial institutions, government agencies, and non-profit organizations. Each of these groups has different needs and pain points that should be addressed in our marketing strategy.

**Key message:** Our key message emphasizes the unique benefits of Alice's Ring solution, which is enhancing privacy, and solvency verification. Giving our users several benefits such as :

-   Protecting Personal Information: Privacy is essential for protecting personal information on the blockchain. By enhancing privacy, users can protect their real identity, transaction history, and other sensitive information from being exposed to third parties.
    
-   Reducing the Risk of Fraud: Enhancing solvency verification can help reduce the risk of fraud on the blockchain. By verifying a user's solvency without disclosing their wallet address or transaction history, it becomes harder for fraudsters to fake or manipulate their financial status.
    
-   Encouraging Adoption: Enhancing privacy and solvency verification can help encourage adoption of blockchain technology. By addressing concerns about privacy and security, more users may be willing to use blockchain-based applications and services.
    
-   Increasing Trust: Enhancing privacy, and solvency verification can also increase trust in the blockchain ecosystem. By providing users with a greater sense of security and control over their information, they may be more willing to engage in transactions and interactions on the blockchain. This can lead to increased trust among users and stakeholders in the blockchain ecosystem, which can ultimately drive greater adoption and usage.
    
**Create Content:** The next step for us will be to create content that resonates with the target audience. This includes blog posts, social media content, case studies, whitepapers, and webinars.

**Attend Conferences and Events:** Attending blockchain and cryptocurrency conferences and events is an effective way to network and connect with potential customers. Our marketing strategy includes a plan to attend relevant conferences and events and showcase Alice's Ring solutions. Our genesis event, ETHDenver, is a perfect exemple.

**Measure Results:** Finally, it's important to measure the results of our marketing strategy. This includes tracking website traffic, social media engagement, lead generation, and conversion rates. Based on the results, the marketing strategy should be adjusted and refined to optimize our results.

## **9.  Product development**

Alice’s ring enhances features that require external technical solutions for front-end and back-end development. Here are the solutions that will be used.

### **Alice's ring - Front End Application**

The front end application in react developed during the ETHDenver 2023 hackathon aims to offer the possibility to interact with the different ring signature functionalities and to issue proof of solvency for different use cases.

#### **Structure :**

**Home page:**
In this section you will learn more about our Alice's ring project and the "proof of solvency" that we can generate and issue thanks to ring signatures. There are many use cases and we have detailed some of them for you.

**ZkBob - Direct Deposit:**
Issuing proof of solvency is the first step before starting the transfer cycle. Indeed, after having attested to his solvency, the user may be required to transfer funds. But this step must not disclose its address and link it to its identity (see use cases). zkBob gives you the freedom to deposit, transfer, and withdraw stable assets privately using zk technology paired with the BOB stablecoin. We have implemented the "Direct Deposit" feature and can find the smart contracts used in our dedicated Github repository.
In order to perform direct deposit actions via our smart contract, the user must first connect to our front end. Several wallets are available: Metamask, WalletConnect, Coinbase Wallet and Rainbow. Currently BOB transfers are only available on Polygon mainnet and the sepolia testnet.

**Technologies used :**

-   React
    
-   Rainbowkit
    
-   wagmi
    
-   Infura RPC provider
    
-   zkBob
  
Thanks to the large number of chains supported, we first used infura's RPCs for Polygon and Ethereum networks (mainnet&testnet). The infura and truffle tools were also useful for the deployment of multi-chain smart contracts. For Scroll and zkSync networks we used the RPCs provided in their respective documentations.

**Supported networks:**
Currently, our application supports several networks but not all of them can be used for the same functionalities.


For the moment, our solutions are available on the following blockchains:

  

### **Solvency proof :**

**Mainnet :**
- Polygon
   
**Testnet :**
-   Scroll Alpha Testnet
-   Polygon ZkEVM
-   Polygon mumbai
-   Goerli
-   Sepolia  

### **ZkBob direct deposit :**

**Mainnet :**
-   Polygon

**Testnet :**

-   Sepolia

Due to ZkBob choices, Direct Deposits can only be performed. Mainnet will be on Polygon and testnet is live and is on Sepolia.

### **Alice's ring - zkBob Direct Deposit smart contract**

BOB is a decentralized stablecoin with opt-in privacy and confidentiality features powered by a protocol based on zk-SNARKs. One of the disadvantages of these types of protocols is the sender needs to calculate a proof using their secret key each time, making it difficult to use a smart contract to automate such payments. This problem is solved by introducing the Direct Deposit feature. You can now send funds to anyone in the privacy pool directly from the smart contract. This feature makes the zkBob protocol much more composable and suitable for integration where funds transfer can be included as a subroutine to other decentralized protocols. See more details in the documentation.

### **Configuration**

We use the React Truffle Box to write, compile, test, and deploy smart contracts, and interact with them from a React app. It's a great tool for every developer, and it helps us a lot during our development journey.

### **Challenges and benefits of using Infura and the Truffle suite of tools**

Our challenges were numerous during the design and implementation of our project.

First we had to create a portable, scalable and understandable development environment for the whole team but also in view of a future reuse of the project by other developers

Our project and our smart contracts must be deployed and usable on different networks (L1, L2). Test, correct, deploy... We needed to have a set of easily usable and implementable tools for these actions.

-   **Convenient access to blockchain networks :** Infura provides convenient access to various networks via L1 and L2 endpoints, so we don't need to set up and maintain our own node and configure our own RPC. This saves us a lot of time and resources, especially during a hackathon.
    
-   Reliable and scalable infrastructure: Infura is built on top of highly reliable and scalable infrastructure, which can help ensure that our dApp remains available and responsive to users.
    
-   Simplified deployment: Using Infura and Truffle box simplify the process of deploying and testing our multichain dApp.
    
-   Integrated with Truffle: Truffle provides built-in support for Infura, so it's easy to configure your Truffle project to use Infura's RPC. The process of RPC configuration inside the truffle-config.js is very simple.
    
-   Truffle for VS Code: As developers we love using VS Code. The Truffle extension for VS Code allowed us to simplify our development process.
    
-   Documentation : The infura and truffle documentation is very detailed and simply explains via concrete examples how to set up your project.
    
    
### **Smart contract architecture**

The goal for our project was to add, with zkBob, the possibility of carrying out private transactions, via a stablecoin, on an EVM chain. zkBob is currently deployed on the Polygon ecosystem, which we particularly appreciate due to its infrastructure and the quality of resources for developers and users. We relied on the zkbob documentation.



**Proof generation :**
( click on the picture to see it clearly )![](https://lh4.googleusercontent.com/j31Gom6gaSTL9QubDfyWFwNiqdN_094Bi_LXkyZA8iJwwlKJ_SK-8oiFxCd7_-fP5ZVZegJF2E7jqYWIWraSUCxgsZpt3w16QSH-WN9izHCKL9IpWgt_tXwky-5pPxkru7DvZZXGxapdOgM7LhJuEDY)

**Direct deposits integration :**

In order to develop the direct deposit functionality, we had to implement the interface IZkBobDirectDeposits.sol within our smart contract. We use the ERC677 transferAndCall approach because it's more gas efficient. Our smart contract interacts directly with the zkBobpool to transfer BOBs from one address to another. To do this the user must allow+deposit BOBs on our "Alice's Ring Direct Deposit '' smart contract. Once done, he has the possibility from our web app to transfer BOBs. One of the advantages of zkBob during our development phase was the good structure of their documentation and the explanations of how their protocol works.

# Why Using Polygon Network:

- High scalability
- Interoperability
- Security
- Developer-friendly
- Community-driven
- Eco-friendly

## High Scalability

Our solution requires fast transaction times that can be enabled by the Polygon's Plasma framework. The optimized version of EVM will enable us to process smart contracts more efficiently, with fast computation and low gas fees.

## Interoperability

- High compatibility with the Ethereum ecosystem (Solidity Language, similar development environment).
- Multiple blockchain networks are supported (Ethereum, BSC…), making good interoperability for our solution.
- Bridges to other blockchain networks for asset transfer and access to a wide range of dApps and services, which is a key aspect of our solution if we want to expand.
- Zkbob is on Polygon and is central to our project. It will allow us to create a micro-ecosystem of privacy transfer and to enable end-to-end anonymous solvency checking.

## Security

Polygon has a strong focus on smart contract auditing and will ensure the safety and security of the smart contracts that we will deploy on the network. Multi-sig is supported by Polygon.

## Developer-friendly

- Significantly low gas fees make it easy for us developers to build and deploy apps on the network.
- SDK includes a range of development tools which provides a simplified interface for interacting with the network.
- We love that the documentation is clear and comprehensive (guides, tutorials, and code samples…)

## Community-driven

- Grants program can really help us since it pushes us and it is designed to encourage community involvement and participation in the network's development.
- Community events and forums will help us network and provide feedback.

## Eco-friendly

We really care about our environmental footprint. The biggest PoW blockchains can consume a yearly quota of anywhere between 35–140 TWh of electricity, with a continuous draw of anywhere between 3–15 GW of electricity. Polygon’s validators approximately consume 0.00079TWh of electricity yearly with an approximate continuous draw of 0.00009GW. Polygon has implemented several carbon offset initiatives, such as partnering with ClimateTrade, to offset the carbon emissions generated by its network operations. This will help us analyze our carbon footprint. Polygon encourages developers to build energy-efficient dApps on the network by providing resources and support for sustainable development practices. That creates an eco-friendly ecosystem that we want to be a part of.


## **10.  Sales Strategies**
    
We aim our solution to be open source. However, the implementation would require some support. This help we provide would be how we generate profit in order to develop and extend. Here are some sales strategies that could be effective for our solution:

### **Targeted Advertising**

Using targeted advertising to reach potential customers who are interested in privacy and solutions for the blockchain. This can include targeting users of existing blockchain applications, social media advertising, and content marketing.


### **Partnerships and Referral Programs**

Establishing partnerships with existing blockchain companies or service providers, and implementing referral programs that incentivize current users to refer new customers to the solution.
 

### **Content Marketing**

Creating valuable and informative content about the solution and the importance of privacy in the blockchain ecosystem. This content can be shared through social media, email marketing, and other digital channels.


### **Public Speaking and Networking**

Engaging in public speaking opportunities, attending conferences and events, and networking with key stakeholders in the blockchain ecosystem to raise awareness about the solution and build relationships with potential customers and partners.


### **Free Trials and Demonstrations**

Offering free trials or demonstrations of the solution to potential customers, allowing them to experience the benefits of the solution firsthand and build trust in the product.  


### **Influencer Marketing**

Collaborating with influencers in the blockchain space who have a significant following and a strong reputation to promote the solution to their audience.


### **Discounts and Promotions**

Offering discounts or promotions for early adopters or for customers who refer new business to the solution can help incentivize customers to try the product and spread the word to others.
  

## **11.  Team**
    
That is the key: the team consists of committed people who love what they do. We are 4 students bound by our passion and commitment for blockchain and Web3. We want to develop innovative solutions that will help the whole ecosystem expand. Too many times have we seen privacy being set aside in projects and we want to be able to change that. That is why Maxime, Nathan, Thomas and Adam are glad to present Alice’s ring, the solution for real privacy.

By addressing the need for privacy in the blockchain ecosystem while having a real utility in our daily life, Alice's Ring has the potential to be a valuable tool for individuals and businesses alike.


## **12.  Technical roadmap**
    
**Q2 2023 :** Implementing Metamask snap code for proof generation; Web app improvement. Deploy and connect to new networks

**Q3 2023 :** Audit and full use case integration: apartment renting, charitable donations, investments

**Q4 2023 :** publishing cryptographic libraries for EVM based “solvency proof” generation and verification

**Q1 2024 :** R&D on zk solvency proof and partnership with a zkRollup


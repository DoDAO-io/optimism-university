## AttestationStation


## Attestations & EAS

### What are Attestations?

Attestations are described as digital signatures of structured data. They play a crucial role in representing trust and identity in digital interactions.They serve as fundamental components of decentralized identity systems. The challenge of numerous identity protocols being developed, leads to fragmentation in the ecosystem. This fragmentation makes it challenging for developers to create a comprehensive view of digital identity. Identity can be represented as an aggregate of attestations made by various entities over time. This means that entities can both receive and issue attestations about themselves, creating a comprehensive picture of their identity.

### What is Ethereum Attestation Service (EAS)?

Ethereum Attestation Service (EAS) is an open-source infrastructure designed to provide a public good for creating attestations. It is intended to serve as a foundational layer for various applications and use cases. EAS is versatile, supporting both on-chain and off-chain attestations. This flexibility allows developers to choose the most suitable approach for their specific needs. It offers an SDK (Software Development Kit) along with a set of developer tools. These tools are designed to simplify the process of working with attestations, making it easier for developers to integrate EAS into their projects. EAS follows a grant-based funding model. This model ensures that EAS remains a public good and is not monetized as part of its infrastructure. The focus is on providing a service to the community rather than generating revenue from the infrastructure itself.

### EAS Contracts

EAS operates using two fundamental smart contracts. These contracts form the foundation of the service's functionality:

<div align="center">
  <img style="max-height:400px;margin-bottom:30px" src="https://d31h13bdjwgzxs.cloudfront.net/academy/optimism-university/Guide/attestationstation_optimism_university_196/1695984058527_untitled-2023-09-21-1651.png"/>
</div>

#### Schema Registry Contract

This contract allows users to register structured data about various topics. It serves as a way to define and categorize the types of data that can be attested to within the EAS ecosystem.

#### Attestation Contract

The second contract enables the creation of attestations based on the registered schemas. It is the core component responsible for generating and managing attestations.

    


---
## Evaluation





##### What are Attestations?  
     
- [ ]  Digital currency used in online transactions
- [x]  Digital signatures of structured data representing trust and identity
- [ ]  Software used for creating digital art
- [ ]  Hardware used for mining cryptocurrencies





##### What is the purpose of Ethereum Attestation Service (EAS)?  
     
- [ ]  To mine Ethereum
- [ ]  To create a new cryptocurrency
- [ ]  To track and monitor cryptocurrency transactions
- [x]  To provide a public good for creating attestations

    


---
## AttestationStation

### What is AttestationStation?

AttestationStation is a crucial component in building decentralized identity applications. It is a smart contract that utilizes the [Ethereum Attestation Service](https://community.optimism.io/docs/identity/atst-v1.html) standard to create, verify, and revoke on/off-chain attestations. Think of AttestationStation as a multiplayer database that streamlines the attestation process and establishes a robust web of trust on any OP Chain in the Superchain.

<div align="center">
  <img style="max-height:400px;margin-bottom:30px" src="https://d31h13bdjwgzxs.cloudfront.net/academy/optimism-university/Guide/attestationstation_optimism_university_196/1695726951931_untitled-2023-09-26-1601.png"/>
</div>

### Advantages of AttestationStation

- **Permissionless**: It is permissionless, meaning it is a public contract not owned or controlled by any individual or organization. 

- **Tooling**: It provides various tooling options such as indexing and access-management integrations, making it convenient for developers. 

- **Flexibility**: If you have a great idea but lack the technical expertise to build it, AttestationStation can be a valuable resource. Attestations also offer benefits over soulbound/non-transferable tokens, such as flexibility in choosing whether the attestation is onchain or offchain and improved interoperability.

### Consideration Using Attestations
When using attestations, it is important to prioritize user privacy. Attestations create log entries that become part of the permanent record on the blockchain. To protect users' privacy, explicit consent should be obtained for collecting personal information. Users should be clearly informed about the data being collected, the purpose of collection, and how it will be used. To ensure data security, sensitive information can be stored offchain using encryption, proper authentication, and authorization measures.

Attestations should not be seen as replacements for verifiable credentials or decentralized identifiers. Instead, they can be used by developers to create decentralized identifiers, credentials, claims, and more. Attestations and the associated web of trust work in conjunction with proof of personhood solutions like WorldID. This combination helps prevent sybil-attacks and provides additional information about a person's reputation, which is crucial in governance and other use-cases. 



    


---
## Evaluation





##### What is AttestationStation?  
     
- [ ]  A software for creating digital art
- [ ]  A tool for online gaming
- [x]  A smart contract for creating, verifying, and revoking attestations
- [ ]  A platform for online shopping





##### What is a crucial consideration when using attestations?  
     
- [ ]  The color of the user interface
- [x]  Prioritizing user privacy
- [ ]  The speed of the internet connection
- [ ]  The cost of the service

    


---
## Optimist Profile

The Optimist Profile is a platform that allows individuals and organizations to showcase their contributions and impact within the Optimism Collective. It is built using onchain reputation data on OP Mainnet and offers various elements to create a comprehensive profile. 

It comprises of the following elements:

### Profile Schema
This is an onchain self-attestation using a profile schema that represents an individual or organization. It provides a standardized format to present information about oneself or one's organization.

### Contributions
Each Optimist Profile can create onchain attestations about their contributions to the Optimism Collective. This means that users can highlight the specific ways in which they have made a positive impact within the community. They can also be used to create onchain peer-to-peer (p2p) attestations about the contributions of other contributors. This helps to establish a web of trust within the Optimism Collective, as individuals can vouch for the contributions of their peers.

The Optimist Profile is built on attestations using the Ethereum Attestation Service. It utilizes specific profile schema and application schema UIDs to store and retrieve relevant information. The profile schema UID represents the profile itself, while the application schema UID represents the specific application being used.

<div align="center">
  <img style="max-height:400px;margin-bottom:30px" src="https://d31h13bdjwgzxs.cloudfront.net/academy/optimism-university/Guide/attestationstation_optimism_university_196/1695647439460_untitled-2023-09-25-1547.png"/>
</div>

[Profile schema UID](https://optimism.easscan.org/schema/view/0xac4c92fc5c7babed88f78a917cdbcdc1c496a8f4ab2d5b2ec29402736b2cf929): ​​0xac4c92fc5c7babed88f78a917cdbcdc1c496a8f4ab2d5b2ec29402736b2cf929

- name: name of the profile
- profileMetadataPtrType: used to determine the protocol
- profileMetadataPtr: can be a URI, ipfs hash, etc. that points to any type of blob storage that stores the metadata


[RetroPGF 3 Application schema UID](https://optimism.easscan.org/schema/view/0x76e98cce95f3ba992c2ee25cef25f756495147608a3da3aa2e5ca43109fe77cc): 0x76e98cce95f3ba992c2ee25cef25f756495147608a3da3aa2e5ca43109fe77cc

- displayName: name of the application
- applicationMetadataPtrType: used to determine the protocol
- applicationMetadataPtr: can be a URI, ipfs hash, etc. that points to any type of blob storage that stores the metadata.


The Optimist Profile offers several benefits to its users. Firstly, it allows individuals and organizations to showcase their contributions and impact within the Optimism Collective, thereby increasing their visibility and recognition within the community. Secondly, the peer-to-peer attestations foster a sense of trust and collaboration among contributors, creating a strong network of support. Lastly, the use of onchain reputation data ensures transparency and authenticity in the information shared on the platform.

    


---
## Evaluation





##### What is the Optimist Profile?  
     
- [ ]  A platform for sharing personal photos and videos
- [x]  A platform to showcase contributions and impact within the Optimism Collective
- [ ]  A platform for online shopping
- [ ]  A platform for video gaming





##### What is the benefit of using the Optimist Profile?  
     
- [ ]  It allows users to share personal photos and videos
- [ ]  It allows users to buy and sell products
- [x]  It allows users to showcase their contributions and impact, fosters trust and collaboration, and ensures transparency and authenticity
- [ ]  It allows users to play online games

    


---
## Schemas

Schemas play a crucial role in AttestationStation as they define the structure and type of data that can be included in an attestation. These schemas act as a blueprint, ensuring that the data included in an attestation is organized and standardized. By following these predefined schemas, the information can be easily understood and processed by different systems.

On OP Mainnet, there are several relevant schemas being used. These schemas are identified by unique addresses:

<div align="center">
  <img style="max-height:400px;margin-bottom:30px" src="https://d31h13bdjwgzxs.cloudfront.net/academy/optimism-university/Guide/attestationstation_optimism_university_196/1695727252990_untitled-2023-09-26-1601.png"/>
</div>

### General Schemas

[Optimist Profile schema UID](https://optimism.easscan.org/schema/view/0xac4c92fc5c7babed88f78a917cdbcdc1c496a8f4ab2d5b2ec29402736b2cf929): ​​0xac4c92fc5c7babed88f78a917cdbcdc1c496a8f4ab2d5b2ec29402736b2cf929

[Gitcoin Passport V1 scores schema UID](https://optimism.easscan.org/schema/view/0x6ab5d34260fca0cfcf0e76e96d439cace6aa7c3c019d7c4580ed52c6845e9c89): 0x6ab5d34260fca0cfcf0e76e96d439cace6aa7c3c019d7c4580ed52c6845e9c89

### RetroPGF Schemas

[RetroPGF Badgeholders schema UID](https://optimism.easscan.org/schema/view/0xfdcfdad2dbe7489e0ce56b260348b7f14e8365a8a325aef9834818c00d46b31b): 0xfdcfdad2dbe7489e0ce56b260348b7f14e8365a8a325aef9834818c00d46b31b

[RetroPGF 3 Application schema UID](https://optimism.easscan.org/schema/view/0x76e98cce95f3ba992c2ee25cef25f756495147608a3da3aa2e5ca43109fe77cc): 0x76e98cce95f3ba992c2ee25cef25f756495147608a3da3aa2e5ca43109fe77cc

[RetroPGF 3 Lists schema UID](https://optimism.easscan.org/schema/view/0x3e3e2172aebb902cf7aa6e1820809c5b469af139e7a4265442b1c22b97c6b2a5): 0x3e3e2172aebb902cf7aa6e1820809c5b469af139e7a4265442b1c22b97c6b2a5

Each schema specifies the structure and type of data that can be included in an attestation, ensuring consistency across different attestations.

The purpose of these schemas is to provide a standardized format for the data included in an attestation. This allows different systems and applications to easily interpret and process the information. By adhering to these schemas, developers can ensure that their attestations are compatible with the existing infrastructure and can be seamlessly integrated into the ecosystem.

AttestationStation v1, the platform used for managing attestations, provides support for these schemas. It allows users to create attestations that adhere to the predefined schemas, ensuring that the data is structured correctly. This simplifies the process of creating and managing attestations, as users can rely on the predefined schemas to guide them.

In addition to providing structure and organization, schemas also contribute to the security and integrity of the attestations. By defining the type of data that can be included, schemas prevent the inclusion of malicious or unauthorized information. This ensures that the attestations are reliable and trustworthy, as they follow a predefined set of rules and standards.

    


---
## Evaluation





##### What role do schemas play in AttestationStation?  
     
- [ ]  They provide the color scheme for the user interface
- [ ]  They determine the pricing of the attestations
- [x]  They define the structure and type of data that can be included in an attestation
- [ ]  They handle user authentication and authorization





##### What is the purpose of schemas in AttestationStation?  
     
- [ ]  To provide a unique identification for each user
- [x]  To provide a standardized format for the data included in an attestation
- [ ]  To provide a platform for users to interact with each other
- [ ]  To provide a method for users to pay for their attestations

    


---
## Examples

Here are some of the applications that utilize the AttestationStation:

### AttestationStation v1

[EAS Scan](https://optimism.easscan.org/): This no-code interface enables you to construct schemas, perform queries, and submit attestations.

<div align="center">
  <img style="max-height:400px;margin-bottom:30px" src="https://d31h13bdjwgzxs.cloudfront.net/academy/optimism-university/Guide/attestationstation_optimism_university_196/1695882682832_untitled-2023-09-28-1116.png"/>
</div>

### AttestationStation v0

[AttestationStation Interface by sbvegan](https://attestationstation.xyz/): This interface allows you to query and submit attestations.

[Optimist Score by Flipside](https://science.flipsidecrypto.xyz/optimist/)

[Optimism Attestor](https://provenance.clique.social/attestor/opattestor) and [ZK Discord Attestations](https://clique.social/attestor/opattestor_discordroles) by Clique: These applications bring web2 user behavior and identity data onto the blockchain, bridging the gap between value-creating activities in web2 and incentive distribution layers in web3.

[Credit Risk Score by RociFi](https://v2.roci.fi/app/analytics?address=0x00227dd82fae1220bdac630297753bb2cb4e8ddd): This application mints NFCS (Non-Fungible Credit Score), offers DeFi Credit Scoring, and supports borrowing under-collateralized DeFi Loans with 70-85% collateral, as well as lending at up to 15% APR.

[Data Provider by Sismo](https://factory.sismo.io/): This application allows you to create a Sismo Connect app or badge for your users.

[Otterspace Score](https://docs.otterspace.xyz/otterspace-attestation-score): Otterspace's non-transferable badge protocol assists dApp builders and communities in creating improved incentive systems, non-financial rewards, and automated permissions.

    


---
## References

https://community.optimism.io/docs/identity/build/

https://community.optimism.io/docs/identity/atst-v1.html

https://optimism.easscan.org/schema/view/0xac4c92fc5c7babed88f78a917cdbcdc1c496a8f4ab2d5b2ec29402736b2cf929

https://optimism.easscan.org/schema/view/0x76e98cce95f3ba992c2ee25cef25f756495147608a3da3aa2e5ca43109fe77cc

https://optimism.easscan.org/schema/view/0x6ab5d34260fca0cfcf0e76e96d439cace6aa7c3c019d7c4580ed52c6845e9c89

https://optimism.easscan.org/schema/view/0xfdcfdad2dbe7489e0ce56b260348b7f14e8365a8a325aef9834818c00d46b31b

https://optimism.easscan.org/schema/view/0x76e98cce95f3ba992c2ee25cef25f756495147608a3da3aa2e5ca43109fe77cc

https://optimism.easscan.org/schema/view/0x3e3e2172aebb902cf7aa6e1820809c5b469af139e7a4265442b1c22b97c6b2a5

    


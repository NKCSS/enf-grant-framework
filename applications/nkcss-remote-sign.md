# EOS Network Foundation Grant Proposal

- **Project Name:** Antelope Remote Sign
- **Team Name:** Nick Kusters Custom Software Solutions
- **EOS Payment Address:** nicknftstash
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3
- **Pomelo Grant(s):** N/A
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/NKCSS/antelope-remote-sign

## Contact

- **Contact Name:** Nick Kusters
- **Contact Email:** enf@nkcss.com
- **Website:** https://nkcss.com/

## Project Overview

### Overview

- **Name:** Antelope Remote Sign
- **Brief Description:** Delegate sigining to a secondary device enabling zero-trust on the platform where you interact with an Antelope chain, like a public PC, Console, Smart TV, you name it.
- **Relationship to EOSIO:** The project will allow any Antelope (formerly EOSIO)-based chain to utilize this system by adding wallet support on the public-facing interface.
- **Reason for Interest:** In the past, trying Unity games that integrated with Antelope chains with FAT clients, requires full trust that there isn't something in the executable that will steal your keys. Similarly, you don't want to have your wallet on untrusted or just a plethora of devices, or, when you want to bring functionality to platforms where wallets just can't run natively.

### Project Details

Have you ever linked your NetFlix account to a Smart TV? The process is fairly easy; go to a special short url, enter 4-5 characters, and boom, your account is linked.

Imagine this, where you can delegate sigining to a different PC or SmartPhone so you don't have to worry about having to sign stuff on-device/in-process.

Example: A Smart TV app, where you can play a game or buy Funko's on your Smart TV, or a Native game client where you don't want to leave the game experience or embed a flow breaking webview to sign things, but have them pop up on your phone or laptop instead.

Example: 

dApp (let's call it Bla) posts request to createlink.doesnotexistyet.com with their app identifier, this returns code: O K D K. 
dApp shows message: "go to doesnotexistyet.com/link and enter code O K D K"
Device capable of signing goes to doesnotexistyet.com/link, enters code "O K D K" and sees: "Would you like to link your wallet to dApp Bla?"
dApp gets a callback with a session identifier that can be used to send requests; can see status of the signer (online/offline)

dApp can now use the session identifier to create new signing requests for the client; the client will see the dApp name and a dialogue will show where they are asked to sign the request from the dApp. When signed, the tx information is sent back to the dApp.

Added benefit is that you no longer need to have a signing wallet on the machine where you try crypto games/apps, etc. Since this has always been a security issue; you no longer have to worry about that. But also, you could integrate into Console games, smart refrigerators, what ever can do a websocket/REST call.

It's also easy to add any kind of wallet support to the remote signing. Additional wallets can be added when needed.

High level overview:

Website where dApps can create a profile (name, image, contact info to show when people link)
REST API to create links, query status and issue requests
WebSocket API for bidirectionally do the same (eliminate polling)
Website where customers can link/sign requests/break the connection (+ WebSocket to get bidirectional notifications about requests)

### Ecosystem Fit

- Where and how does your project fit into the ecosystem?

It can be integrated like you'd integrate a new wallet provider for dApps; and on the execution side, you can implement all the various wallet providers. This, in theory, could also replace something like UAL where you'd just implement the remote sign solution and all the other stuff is abstracted away.

- Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?

Mostly Desktop/Console games, but this would be a benefit to every dApp.

- What need(s) does your project meet?

Added security layer and bringing Antelope to places where it could not go before.

- Are there any other projects similar to yours in the EOSIO ecosystem?

Not that I'm aware of

## Team

### Team members

- **Team Leader:** Nick Kusters

### Legal Structure
- **Registered Legal Entity:** Nick Kusters Custom Software Solutions
- **Registered Address:** Pletzersstraat 32, 6213HH Maastricht, The Netherlands

### Team Experience

28 years of coding experience, 22 of that professionally, former CTO at a startup, building Wax Smart Contract & Tools for projects for 18 months.

I have videos about some of the things I've built on Wax on [nick.yt](https://nick.yt)

Some other videos: 
- [Thee Hustle House Interview](https://www.youtube.com/watch?v=GrYxezXDg9g&feature=emb_imp_woyt)
- [Thee Hustle House showcasing my R-Planet tool](https://www.youtube.com/watch?t=434&v=FzdKltTE7jQ&feature=emb_imp_woyt)
- [Zueljin showing my Alien Worlds tools](https://www.youtube.com/watch?t=544&v=mn2HBehAOik&feature=emb_imp_woyt)
- [Uplift talks about my tools](https://www.youtube.com/watch?t=1965&v=OrcGvVkbvGg&feature=emb_imp_woyt)
- [Bonz & Anders talk about my R-Planet tools](https://www.youtube.com/watch?t=981&v=lq3O1t7oC-0&feature=emb_imp_woyt)

### Team Org Repos

- https://github.com/NKCSS/ABI2CSharp

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/nick-kusters-0a78418/

## Development Status

Not started yet

## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:** 3 months
- **Full-Time Equivalent (FTE):** 1 FTE
- **Total Costs:** 58,360 USD

### Milestone 1 — Server hosting & management for a year

- **Estimated duration:** 1 week
- **FTE:** 1
- **Costs:** 6,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | N/A |
| 0b. | Documentation | We will provide a basic **tutorial** that explains how a user can set up a server. |
| 0c. | Testing Guide | N/A |
| 1. | Rent server for a year |  
| 2. | Buy domain for a year |  
| 3. | Set up NGINX, .NET Core & Let's Encrypt |

### Milestone 2 — Smart contract to register/authenticate dApps

- **Estimated Duration:** 2 weeks
- **FTE:**  1
- **Costs:** 10,880 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | all rights preserved |
| 0b. | Documentation | We will provide **inline documentation** of the code |
| 0c. | Testing Guide | Testing will be done through the various interfaces that interact with the smart contract |
| 1. | Smart Contract | We will create a smart contract that lets dApps register and provide information about the dApp that can be used to display to the client when linking/sigining requests |  

### Milestone 3 — REST API

- **Estimated Duration:** 3 weeks
- **FTE:**  1
- **Costs:** 14,280 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | all rights preserved |
| 0b. | Documentation | We will provide **inline documentation** of the code and a **tutorial** for dApps how to interact |
| 0c. | Testing Guide | Testing will be done through the various interfaces that interact with the smart contract |
| 1. | Register API | Create a REST api for dApps to register a display name, description and ipfs hash to show when users link their wallet/get a signing request as well as register a webhook where sign notifications can be posted to to prevent the need for long polling. |  
| 2. | Sign Request API | Lets dApp request a **link** code to establish a communications channel to request remote sigining of transaction and poll for status updates for those who want to verify/can't implent webhooks. |
| 3. | Webhook | Implement the webhook logic |

### Milestone 4 — Website UI/UX where customers can link/sing request/unlink

- **Estimated Duration:** 3 weeks
- **FTE:**  1
- **Costs:** 13,600 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | all rights preserved |
| 0b. | Documentation | We will provide **inline documentation** of the code and a **tutorial** for customers how to interact |
| 0c. | Testing Guide | Test script document will be created with functionality and what to expect |
| 1. | Website | Mobile first design, incorporate on-chain settings from the dApps |
| 2. | Styling | Light & Dark theme (auto-sense platform settings + manual override) |
| 3. | Manage wallets | If the user has not linked any wallets, ask them to do so (functinality won't exist yet when this will get built), add a button to the UI where you can manage your wallets (add/remove; destroying existing links). |
| 4. | Link | Show linq request, let user link (choose a linked wallet, interact with API, which will call webhook with link result/have the info ready to be polled) |
| 5. | Unlink | Let clients destroy their link (interact with API, which will call webhook with link result/have the info ready to be polled) |
| 6. | Sign | Show a triggered sign request from a dApp |

### Milestone 5 — WebSocket API for Dapp

- **Estimated Duration:** 2 week
- **FTE:**  1
- **Costs:** 6,800 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | all rights preserved |
| 0b. | Documentation | We will provide **inline documentation** of the code and a **tutorial** for dApps how to interact |
| 0c. | Testing Guide | Test page to call actions; manually verify |
| 1. | WebSocketAPI | Two-way API to do the same as the REST API without the need to poll/receive webhook, making the interactions faster |

### Milestone 6 — WebSocket API for Client-facing website

- **Estimated Duration:** 1 week
- **FTE:**  1
- **Costs:** 4,080 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | all rights preserved |
| 0b. | Documentation | We will provide **inline documentation** of the code |
| 0c. | Testing Guide | Test page to call actions; manually verify |
| 1. | WebSocketAPI | This will be the main driver for the Client-Facing website, receive signing requests, post the responses which then get fed to the webhook and dApp websocket api |

### Milestone 7 — Integrate Anchor as the Pilot wallet

- **Estimated Duration:** 1 week
- **FTE:**  1
- **Costs:** 2,720 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | all rights preserved |
| 0b. | Documentation | We will provide **inline documentation** of the code |
| 0c. | Testing Guide | Test page to call actions; manually verify |
| 1. | Integrate Anchor | Since anchor works for a lot of Antelope chains, this was the wallet provider I wanted to start with. In a later stage, more can be added. |


## Future Plans

When the project is completed, I plan to also apply for a wax labs grant to add WCW as an additional wallet provider.

## Additional Information

**How did you hear about the Grants Program?** personal recommendation by Kaefer

**Other Antelope projects I've done**:
- Monitor Wax CPU usage, RAM price, orgn.wax queue, chain CPU pressure and your CPU stake, execute raw transactions, view & claim balances (also available for testnet): https://wax-tools.naw.io/ 
- Crystalize FTs to NFTs (and back again): https://wax-tools.naw.io/crystalize.html
- R-Planet income calculator, WCW tokens tool, claim tool, element information, Land information and ticket information: https://rp.naw.io/
- ClashDome WCW Token, Land income claim tool & notification system: https://rp.naw.io/
- BluDac WCW token tool: https://bd.naw.io/
- Metal War custom auth key creator / MECH <-> SHARD converter: https://mw.naw.io/
- Alien Worlds: Notification system for when you are awarded an NFT, claim system for NFTs, change bag tool: https://aw.naw.io/
- Farming Tales: External market to buy game NFTs with in-game tokens: https://ft.naw.io/
- Telegram & Twitter Bot for Alien Worlds Planet Binance mission notifications: https://twitter.com/AWMissionBot
- Mining Network Telegram bot to spit out more acurate information: https://t.me/NicksTechdom
- NFT Exchange (linked to Wax Testnet at the moment): https://waxpx.com
- Build the smart contracts for https://market.anyo.io/ to gather information required to file NFT sales taxes in Sweden for Anyobservation, linking to auto-whitelisting verified accounts to drops.
- Helping the 7th seal team build smart contract: https://www.the7thsealgame.com/post/developer-update-2022-01-28
- Got a Wax Labs grant to build ABI2CSharp; a developer utility that let's you quickly interact with any Antelope chain from C#: https://labs.wax.io/proposals/88
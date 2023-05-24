# [Picasarts contracts](https://github.com/neitdung/picasarts-contracts)

## Install
Prerequites: [hardhat](https://hardhat.org/hardhat-runner/docs/getting-started#overview) 

- Clone repository: [picasarts-contracts](https://github.com/neitdung/picasarts-contracts)
- Install modules: ```npm install```
- Compile contracts: ```npx hardhat conpile```
- Config network in file: ```hardhat.config.js```
- Deploy contracts: ```npx hardhat run --network <network> scripts/deploy_all.js```
- Get file ```config.json``` and all files in folder ```abis```

## Design

Picasarts has 1 governance contract (Hub) and 3 feature contracts (Marketplace, Loan and Rental). For handle logic of feature contracts and futher extending contract, this is design of them:

![Smart contracts design](../imgs/main-sc.png)

Those also use same a NFT standard contract called PNFT extend from ERC-721, ERC-2981 and ERC-4907. This is not required, you can create new PNFT contract by Hub or just import simple ERC-721 contract that extend Ownable contract but I encourage you use this contract for able using full product features.

![PNFT](../imgs/pnft.png)

## Use cases and flow

![All usecase](../imgs/all-uc.png)

### Hub

![Hub](../imgs/hub-uc.png)

### Marketplace

- Use cases:
![Market use cases](../imgs/market-uc.png)
- Flow:
![Market flow](../imgs/market-fl.png)

### Loan

- Use cases:
![Loan use cases](../imgs/loan-uc.png)
- Flow:
![Loan flow](../imgs/loan-fl.png)
- Explain status after each action:
![Loan explain](../imgs/loan-expl.png)

### Rental

- Use cases:
![Rental use cases](../imgs/rent-uc.png)
- Flow:
![Rental flow](../imgs/rent-fl.png)
- Calculate amount can withdraw:
![Rental explain](../imgs/rent-expl.png)
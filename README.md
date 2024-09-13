<div id="top"></div>

<!-- ABOUT THE PROJECT -->

## Decentralized Marketplace App

This is a decentralized marketplace built for EVM compatible blockchains, it enables sellers and buyers from all around the world to buy and sell their products in secure and trustless manner, and even thought products are listed in $ (to avoid the volatility of the crypto market) all the payment are done using cryptocurrencies (ETH, MATIC,...) and all the purchase steps are controled by the MarketPlace smart contract logic.

### Built With

- [Solidity](https://docs.soliditylang.org/)
- [Brownie](https://eth-brownie.readthedocs.io)
- [React.js](https://reactjs.org/)
- [ethers.js](https://docs.ethers.io/v5/)
- [web3modal](https://github.com/Web3Modal/web3modal)
- [material ui](https://mui.com/getting-started/installation/)

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#how-it-works">How it Works</a></li>
    <li>
      <a href="#usage">How to Use</a>
      <ul>
        <li><a href="#contracts">Contracts</a></li>
        <li><a href="#scripts">Scripts</a></li>
        <li><a href="#testing">Testing</a></li>
        <li><a href="#front-end">Front End</a></li>
      </ul>
    </li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#license">License</a></li>
  </ol>
</details>

<!-- GETTING STARTED -->

## Getting Started

### Prerequisites

Please install or have installed the following:

- [nodejs and npm](https://nodejs.org/en/download/)
- [python](https://www.python.org/downloads/)
- [MetaMask](https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn) Chrome extension installed in your browser

### Installation

1. Installing Request: Request is a node module that enhances the development, testing, and deployment of smart contracts, particularly for those who prefer to use JavaScript for writing their scripts. It complements Truffle by providing a streamlined experience for managing your smart contract workflows.
   Here is a simple way to globally install request.
   ```bash
   npm i -g request
   ```
2. Clone the repo:

```bash
  git clone https://gitlab.com/plusblue/marketplace-dapp.git
  cd marketplace-dapp
```

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- Working EXAMPLES -->

## How it Works

Decentralized marketplaces are one of the best use cases of blockchains technologies. They allow people to interact and transact on a global, permission-less, and self-executing platform. Houses, hot sauce, and t-shirts can all be bought and sold without needing to trust a middleman and with smaller fees.

The application allow any user to add a product by providing the product name, description, price in $ and image.

The platform ensures a good interaction between the seller and the buyer by deviding the purchase process (product state) into 4 steps:

  <ul>
    <li><b>In Sale:</b> The first step when a seller list it's product on the market </li>
    <li><b>Pending:</b> When a product is bought the amount paid is locked in the smart contract and buyer waits for seller to sent the product </li>
    <li><b>Sent:</b> The seller sends the product and waits for the buyer confirmation</li>
    <li><b>Sold:</b> The buyer confirms the recieval and the funds are transfered to the seller </li> 
  </ul>
 
All this steps can be performed on the product page:

<b>Seller point of view: </b>

<b>Buyer point of view: </b>

The user can find the list of products he is selling and that he is buying on the My product page:

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->

## How to Use

### Contracts

The app is based on a single global contract called MarketPlace, it contains the following functions :

  <ul>
    <li><b>Admin functions:</b> Allow admin to change the fee charged for selling a product</li>
    <li><b>Seller functions:</b> Allow a seller to add it's product, change it's price and sent it to the buyer </li>
    <li><b>Buyers functions:</b> Allow buyer to purchase and confirm the recieval of any product </li>
    <li><b>Chainlink Price Feed:</b> the contract uses the price feed provided by chainlink oracle for converting the products prices from $ to ETH </li>   
  </ul>

<p align="right">(<a href="#top">back to top</a>)</p>
    
### FullStack
   The user interface of this application is build using React JS, it can be started by running: 
   ```sh
    npm start
   ```
   It uses the following libraries:
      <ul>
        <li><b>Ethers.js:</b> used as interface between the UI and the deployed smart contract</li>
        <li><b>Web3modal:</b> for conecting to Metamask</li>
        <li><b>ipfs-http-client:</b> for connecting  and uploading files to IPFS </li>
        <li><b>@reduxjs/toolkit & redux-persist:</b> for managing the app states (account, balance, blockchain) </li>
        <li><b>Material UI:</b> used for react components and styles </li>    
      </ul>
      
   The files are structured as follows:
    <ul>
      <li><b>pages:</b> Contains all the app views (MarketPage, ProductPage,...)</li>
      <li><b>Components:</b> Contains all the app component(main, navbar, Account,...) </li>
      <li><b>features:</b> contains the redux toolkit reducer and actions </li>
      <li><b>artifacts:</b> contains all the smart contract data and addresses transfered earlier </li>
      <li><b>NetworksMap:</b> a json file for some known blockchains names & chain id </li> 
    </ul>

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- LICENSE -->

## License

Distributed under the MIT License. See `LICENSE` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>

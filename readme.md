# Decentralized Escrow Application

Welcome to the Decentralized Escrow Application! This project combines a Solidity-based smart contract with a React frontend, allowing users to create and manage escrow transactions on the Ethereum blockchain. 

## Getting Started

### Step 1: Cloning the Repository

To begin, clone the project repository:

```sh
git clone https://github.com/alchemyplatform/escrow-hardhat.git
```

Alternatively, if you don't have Git installed, download a zip of the repository from [here](https://github.com/alchemyplatform/escrow-hardhat.git) and unzip it into a directory on your machine.

### Step 2: Installing Dependencies

Navigate to the root directory of the Escrow project and install the node dependencies:

```sh
cd path/to/escrow/folder && npm install
```

Then, navigate to the React frontend directory and install its dependencies:

```sh
cd app && npm install
```

### Step 3: Running a Local Test Blockchain

To test the application locally, start a local blockchain using Hardhat:

```sh
npx hardhat node
```

This will create a local blockchain with network id 31337 and provide you with several test accounts preloaded with 10000 ETH each.

### Step 4: Install Apex Wallet & Add a Custom RPC Network

Install the Apex Wallet extension for your browser from [here](https://apexwallet.com).

Configure Apex Wallet to connect to your local blockchain:
1. Select the profile dropdown in the top left corner.
2. Select "Import with Private Key" and paste a private key from one of the accounts provided by Hardhat.

### Step 5: Compile the Smart Contract

Compile the Escrow Smart Contract using Hardhat:

```sh
npx hardhat compile
```

This will compile the contract and output the ABI and bytecode in the `/app/src` directory.

### Step 6: Run the Front-End with React

To start the React frontend, navigate to the `/app` directory and run:

```sh
npm start
```

Open [http://localhost:3000](http://localhost:3000) in your browser to view the application.

## Interact with Your dApp

### Creating an Escrow Contract

1. Enter the arbiter, beneficiary, and deposit amount (in Ether) into the provided input fields.
2. Click "Deploy" to create a new escrow contract.
3. Approve the transaction in the Apex Wallet popup.

### Approving the Escrow as the Arbiter

Switch to the arbiter's address in Apex Wallet and approve the transaction. Only the arbiter can call the `approve` function.

## Implemented Challenges

### Challenge 1: Running the dApp on a Live Testnet

The Escrow dApp has been successfully deployed and tested on the Göerli testnet. 

Steps to achieve this:
1. **Alchemy Endpoint**: Acquired an Alchemy endpoint for the Göerli testnet.
2. **Testnet Ether**: Obtained testnet ETH from Alchemy's Göerli Faucet.
3. **Deployment**: Modified the deployment script to target the Göerli network and deployed the contract.
4. **Apex Wallet Configuration**: Configured Apex Wallet to point to the Göerli testnet and interacted with the contract as on the local network.

### Challenge 2: Stylizing the Application

Enhanced the visual appeal and user experience of the dApp.

Changes made:
1. **HTML and CSS**: Redesigned the user interface with improved HTML structure and custom CSS styling.
2. **JavaScript Enhancements**: Added interactive elements and improved form validations.

### Challenge 3: Wei to Ether Conversion

Updated the application to handle Ether instead of Wei for deposits.

Steps taken:
1. **Conversion Logic**: Implemented conversion logic in the application code to convert Ether to Wei before deploying the contract.
2. **User Interface**: Modified the input fields to accept Ether amounts directly, enhancing user-friendliness.

### Challenge 4: Persistence

Implemented a persistence layer to track and display all deployed Escrow contracts, maintaining state across page refreshes.

Approach:
1. **Backend Server**: Developed a simple backend server to store the addresses of deployed Escrow contracts.
2. **Frontend Integration**: Integrated the frontend with the backend to fetch and display the list of deployed contracts on page load.

### Challenge 5: Additional Features

Added new functionalities to the Escrow contract and frontend.

Enhancements:
1. **Multi-Sig Approval**: Implemented multi-signature approval functionality in the smart contract to increase security for large transactions.
2. **Improved Arbitration**: Added logic for automated arbitration based on external proofs of delivery, reducing the reliance on a single arbiter.

## Further Research

Consider exploring additional mechanisms for arbitration or other features to enhance the security and usability of the Escrow application. Potential ideas include decentralized arbitration using DAOs or integrating off-chain data for automated decision-making.

## Conclusion

This project provides a robust foundation for a decentralized escrow application. The additional challenges have been implemented to extend its functionality and improve the user experience. Continue to explore, enhance, and build upon this project to create the best escrow dApp the world has ever seen! 🚀
# hello-hedera-js-sdk

This project demonstrates how to interact with the Hedera Hashgraph testnet using the Hedera JavaScript SDK. The code walks through setting up an environment, creating a new account, verifying balances, and transferring HBAR tokens.

## Prerequisites

Before you can run this project, you need the following:

- Node.js (version 14 or higher)
- npm (Node package manager)
- A Hedera testnet account with its corresponding Account ID and Private Key
- [Hedera JavaScript SDK](https://github.com/hashgraph/hedera-sdk-js)

## Getting Started

1. **Clone the repository:**

   ```bash
   git clone https://github.com/Daslaw/hello-hedera-js-sdk.git
   cd hello-hedera-js-sdk
   ```

2. **Install dependencies:**

   Run the following command in the root directory to install required packages:

   ```bash
   npm install
   ```

3. **Environment Setup:**

   You will need to create a `.env` file in the root directory and provide your Hedera account ID and private key:

   ```bash
   touch .env
   ```

   In the `.env` file, add the following:

   ```bash
   MY_ACCOUNT_ID=<your-hedera-account-id>
   MY_PRIVATE_KEY=<your-private-key>
   ```

   Replace `<your-hedera-account-id>` and `<your-private-key>` with the values from your Hedera account.

4. **Run the Project:**

   To run the script, use:

   ```bash
   node index.js
   ```

## How It Works

1. **Environment Setup**:  
   - The script reads the Hedera Account ID and Private Key from the `.env` file.
   - It connects to the Hedera testnet and sets up the client with the necessary credentials.

2. **Account Creation**:  
   - A new ED25519 key pair is generated.
   - A new account is created with 1,000 tinybars as the starting balance.

3. **Balance Verification**:  
   - The account balance for the newly created account is retrieved and displayed in the console.

4. **Transfer Transaction**:  
   - HBAR is transferred from the original account to the newly created account.
   - The transaction status is confirmed and printed in the console.

## Dependencies

- [dotenv](https://www.npmjs.com/package/dotenv): Loads environment variables from a `.env` file.
- [@hashgraph/sdk](https://www.npmjs.com/package/@hashgraph/sdk): The Hedera JavaScript SDK for interacting with Hedera Hashgraph.

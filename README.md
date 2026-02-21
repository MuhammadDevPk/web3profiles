# Web3 Profiles 🌐

Welcome to **Web3 Profiles**, a modern decentralized profile management dashboard built with Next.js. This application empowers Web3 users to seamlessly manage their decentralized identities, NFT passports, and connect their internal platform assets to their personal Web3 wallets.

## 📖 What is this?

Web3 Profiles is a sleek, responsive web application framework designed specifically for the Web3 ecosystem. It provides a user-friendly interface for individuals to view and edit their blockchain-based profiles, visualize their NFT passports, and handle internal token (`N2DR`) transfers.

## 🚀 What does this do?

- **Decentralized Profile Management**: Users can update their core profile information including First Name, Last Name, Username, and Email.
- **IPFS Avatar Uploads**: Update profile avatars designed to be stored directly on the InterPlanetary File System (IPFS) for true decentralized availability.
- **NFT Passport Integration**: Displays the user's NFT Passport details, rendering their unique Web3 ID and Rank within the platform ecosystem.
- **Wallet & Token Management**: Allows users to dynamically link a new personal Web3 wallet and features a mechanism to transfer internal platform tokens (`N2DR`) out to their personal crypto wallet.

## 🤔 Why use it?

- **For Users**: It simplifies the otherwise complex management of decentralized identity and crypto assets by housing everything in one intuitive, beautifully designed dashboard.
- **For Developers**: This project serves as an excellent starting point or reference implementation for integrating Next.js with core Web3 technologies like `ethers.js`, `web3modal`, and `ipfs-http-client`. It demonstrates how to structure a clean, dark-themed UI that is ready to interact with blockchain data and decentralized file storage.

## 🛠️ Expertise & Value

This project demonstrates strong expertise in bridging modern frontend frameworks with Web3 infrastructure, showcasing:

- **Frontend Architecture**: Built on the robust Next.js 16 App Router (React 19) for optimal performance and fast page loads.
- **Web3 Integration Readiness**: Pre-configured with essential Web3 libraries including Ethereum communication via `ethers.js` and wallet-connection flows via `web3modal`.
- **Decentralized Storage**: Integrated with `ipfs-http-client`, ready to upload and pin user assets (like avatars) to IPFS natively.
- **Modern UI/UX**: Utilizing a blend of customized Bootstrap 5 and Tailwind CSS (`@tailwindcss/postcss`) to provide a premium, gradient-infused dark mode aesthetic, establishing a professional and trustworthy standard typical of high-end Web3 decentralized applications (dApps).

## 💻 How to use it & Prerequisites

### Prerequisites

Before you begin, ensure you have the following installed on your local machine:

- [Node.js](https://nodejs.org/) (v18 or newer recommended)
- A package manager like npm, yarn, pnpm, or bun.
- A Web3 Wallet extension (like MetaMask, Phantom, or Coinbase Wallet) installed in your browser for testing wallet interactions.
- **Optional**: An IPFS node or Infura/Pinata API keys if you plan to fully test and execute the avatar upload functionality.

### Local Setup & Installation

1. **Clone the repository** (or navigate to the project directory):

   ```bash
   cd web3profiles
   ```

2. **Install the dependencies**:

   ```bash
   npm install
   # or
   yarn install
   # or
   pnpm install
   ```

3. **Run the local development server**:

   ```bash
   npm run dev
   # or
   yarn dev
   ```

4. **Access the application**:
   Open [http://localhost:3000](http://localhost:3000) with your browser to view the application. The main interface structure is located in `src/app/page.js`.

## 🧪 Complete Guide to Test it in Code

To test, execute, and build upon this application, follow these developer guidelines:

1. **UI/UX Modifications**:
   - The primary dashboard layout and markup are located in `src/app/page.js`.
   - Global styles and customized CSS variables are found in `src/app/globals.css` and `src/app/styles/custom.css`.
   - The wrapping `<html>` and Next.js font optimizations (Geist) are managed inside `src/app/layout.js`.

2. **Implementing Web3 Logic**:
   - The current `page.js` provides the structural UI. To make it functional, convert it to a Client Component by adding `"use client";` at the very top of `src/app/page.js`.
   - Import and initialize `ethers` and `web3modal` to manage the wallet connection state within React hooks (`useState`, `useEffect`).
   - Bind the input fields (First name, Last name, etc.) to React state to actively capture and utilize user input.

3. **Testing IPFS Uploads**:
   - In `page.js`, locate the profile picture upload input: `<input type="file" name="Asset" />`.
   - Create an `onChange` handler that reads the selected file, creates an instance of `ipfs-http-client`, uploads the buffer to the IPFS network, and retrieves the resulting unique CID.

4. **Testing Token Transfers**:
   - Attach an `onClick` event handler to the **"Transfer N2DR"** button.
   - Write an async function that creates a contract instance using `new ethers.Contract(contractAddress, ABI, signer)`.
   - Call the smart contract's transfer function and await the transaction receipt, displaying success or error messages on the UI (e.g., inside the `<h6 id="displaytransfer" />` element).

## 🤝 Contributing

Contributions, issue identification, and feature requests are very welcome! If you want to improve the codebase, feel free to fork the repository and submit a pull request.

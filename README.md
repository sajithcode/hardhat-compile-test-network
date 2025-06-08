````markdown
# Hardhat Tutorial

This guide walks you through setting up a Hardhat project, compiling a smart contract, testing it, and deploying it to a network such as Hardhat's local node or a public testnet like Sepolia.

---

## 1. Setting Up the Project

First, create a new directory for your project, navigate into it, and initialize a Node.js project. Then install Hardhat as a development dependency.

```bash
mkdir hardhat-tutorial
cd hardhat-tutorial
npm init -y
npm install --save-dev hardhat
````

---

## 2. Creating a Hardhat Project

Run the following command to initialize a new Hardhat project. Choose "Create a basic sample project" when prompted.

```bash
npx hardhat
```

This will generate a directory structure with `contracts/`, `scripts/`, and `test/` folders.

---

## 3. Compiling Your Smart Contract

Compile the sample contract (e.g., `Lock.sol`) located in the `contracts/` directory.

```bash
npx hardhat compile
```

Upon successful compilation, an `artifacts/` directory will be created containing the compiled contract's ABI and bytecode.

---

## 4. Testing Your Smart Contract

Run the tests provided in the `test/` directory.

```bash
npx hardhat test
```

This command will execute the test scripts and display pass/fail results.

---

## 5. Checking Account Balances

### Start the Local Hardhat Node

```bash
npx hardhat node
```

### In a Separate Terminal, Run a Script

```bash
npx hardhat run scripts/sample-script.js
```

### Or Use the Hardhat Console

```bash
npx hardhat console
```

Then, within the console:

```javascript
hre.ethers.provider.getBalance(hre.ethers.provider.getSigner(0).getAddress())
```

---

## 6. Deploying Your Smart Contract

### To Local Hardhat Network

```bash
npx hardhat run scripts/deploy.js
```

### To Ethereum Testnet (e.g., Sepolia)

1. Configure `hardhat.config.js` with:

   * Your testnet RPC URL (e.g., from Alchemy or Infura)
   * Your wallet private key

2. Deploy to the testnet:

```bash
npx hardhat run scripts/deploy.js --network sepolia
```

> 🔁 Replace `sepolia` with your desired network name as configured.

---

## Final Notes

These are the essential terminal commands and steps covered in the Hardhat tutorial. For more advanced usage, refer to the official [Hardhat documentation](https://hardhat.org/).

Happy Building! 🚀

```


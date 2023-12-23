# BankAccount 

## Overview

This is a simple Ethereum smart contract named BankAccount, designed to manage bank account functionalities on the blockchain. It includes features such as opening an account with an initial deposit, checking eligibility for a credit card, and ensuring that only the owner of the contract can perform certain actions.

## Smart Contract Details

### State Variables

- `owner`: The Ethereum address that owns the bank account.
- `balance`: The current balance in the bank account.
- `age`: The age of the account owner.
- `creditScore`: The credit score of the account owner.

### Modifiers

- `onlyOwner`: A modifier that restricts the execution of a function to only the owner of the contract.
- `eligibleForCreditCard`: A modifier that ensures the account owner has a credit score greater than 700.

### Constructor

- Initializes the contract with an initial owner address and a default credit score of 0.

### Functions

1. **openAccount**
   - **Parameters**: `_initialDeposit` (uint256), `_age` (uint256)
   - **Description**: Allows an account to be opened with a specified initial deposit and age. The age must be at least 21, and the initial deposit must be greater than or equal to 5000.

2. **applyForCreditCard**
   - **Parameters**: `_creditScore` (uint256)
   - **Description**: Allows the account owner to apply for a credit card by providing a credit score. The function checks eligibility (credit score > 700) and returns a boolean indicating success.

## Usage

1. **Deploying the Contract:**
   - Deploy the smart contract on the Ethereum blockchain.

2. **Opening an Account:**
   - Call the `openAccount` function with the desired initial deposit and age.

3. **Applying for a Credit Card:**
   - Call the `applyForCreditCard` function with the desired credit score.

4. **Accessing Account Information:**
   - View the `owner`, `balance`, `age`, and `creditScore` variables to retrieve account information.

5. **Owner-Specific Actions:**
   - Ensure that actions requiring ownership are executed by the owner account.

## Modifiers and Security

- The `onlyOwner` modifier adds an additional layer of security by allowing only the owner to perform certain actions.
- The `eligibleForCreditCard` modifier ensures that the account owner meets the credit score eligibility criteria for applying for a credit card.

## Disclaimer

- This smart contract is provided as-is, and users are encouraged to review and test it thoroughly before deploying it on the Ethereum blockchain.
- The contract might need additional features and security measures based on specific use cases and requirements.

## License

This smart contract is licensed under the MIT License. See the provided license file for details.

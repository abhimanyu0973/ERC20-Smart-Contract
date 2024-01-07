## Group members:
Aaditya Mahesh Rathi  2020A7PS2191H
Abhimanyu Gautam      2020A4PS0973H
Shreyas Yogesh Dixit  2020A7PS2079H

# XYZToken and XYZBusinessLogic Contracts

These are two Ethereum smart contracts written in Solidity: XYZToken and XYZBusinessLogic. XYZToken is an ERC-20 token contract, and XYZBusinessLogic is a contract for handling business logic and product purchases using the XYZToken.

## XYZToken Contract

### Description
XYZToken is an ERC-20 token contract with additional functionality to allow the owner to approve spenders and implement a burn feature for token reduction. This token serves as the currency for making purchases in the XYZBusinessLogic contract.

### Functions

#### `constructor(uint256 _initialSupply)`
- Initializes the token with the given initial supply.

#### `approveSpender(address spender, uint256 value)`
- Allows the owner to approve another address to spend tokens on their behalf.

#### `burn(address x, uint256 amount)`
- Allows token burning by reducing the token balance of an address.

#### `validatePurchase(uint256 purchaseAmount, uint256 numberofTokens, uint256 userTokens)`
- Validates purchase parameters to ensure they meet certain criteria.

## XYZBusinessLogic Contract

### Description
XYZBusinessLogic is a contract that allows users to interact with the XYZToken to make purchases. It offers features such as adding products and calculating discounts based on the number of tokens held by the user.

### Functions

#### `constructor(address _tokenAddress)`
- Initializes the contract with the address of the XYZToken contract.

#### `addProduct(string memory _productName, uint256 _price)`
- Allows the owner to add products with their respective prices.

#### `getProductPrice(string memory _productName)`
- Retrieves the price of a specific product.

#### `purchaseProduct(uint256 amount, uint256 numberofTokens)`
- Handles product purchases by applying discounts and transferring tokens and ether between users and the owner.

#### `getCustomerTokenBalance()`
- Retrieves the token balance of the calling customer.

#### `getCustomerBalance()`
- Retrieves the ether balance of the calling customer.

#### `getOwnerBalance()`
- Retrieves the ether balance of the owner.

#### `getAllowance()`
- Retrieves the allowance for the contract to spend tokens on behalf of the owner.

### Modifiers

#### `onlyOwner`
- Ensures that only the owner can perform certain actions in the contract.

## Usage
You can deploy these contracts to the Ethereum blockchain and interact with them using web3 or any Ethereum wallet.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

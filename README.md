# EduCoin

EduCoin is a simple  token implemented in Solidity, designed for educational purposes. This smart contract allows the minting and burning of tokens to represent educational credits awarded to and redeemed by students.

## Features

- **Token Details**: The token is named "EduCoin" with the abbreviation "EDC".
- **Minting**: Award educational credits to students.
- **Burning**: Redeem educational credits from students.
- **Balance Tracking**: Use of mapping to keep track of each student's balance.

## Contract Details

- **Token Name**: `EduCoin`
- **Token Abbreviation**: `EDC`
- **Total Supply**: The total number of EduCoins in circulation.
- **Balances**: A mapping to track the balance of EduCoins for each student.

## Mapping

In this contract, a mapping is used to associate each student's address with their balance of EduCoins. This allows efficient and straightforward tracking of how many EduCoins each student holds.

```solidity
mapping(address => uint) public balances;
```

- `address`: The address of the student.
- `uint`: The number of EduCoins that the student holds.

## Functions

### mint

The `mint` function awards educational credits to a student. This function increases the total supply of EduCoins and updates the balance of the specified student.

```solidity
function mint(address _student, uint _credits) public
```

- `address _student`: The address of the student receiving the credits.
- `uint _credits`: The number of educational credits to award.

### burn

The `burn` function redeems educational credits from a student. This function decreases the total supply of EduCoins and updates the balance of the specified student.

```solidity
function burn(address _student, uint _credits) public
```

- `address _student`: The address of the student redeeming the credits.
- `uint _credits`: The number of educational credits to redeem.

## Usage

To use this contract, deploy it on the Ethereum blockchain using Remix or another Solidity development environment. Once deployed, you can call the `mint` function to award credits to students and the `burn` function to redeem credits.

### Example

Deploy the contract and then call the `mint` function:

```solidity
mint(0xStudentAddress, 100);
```

This will award 100 EduCoins to the student at `0xStudentAddress`.

To redeem credits, call the `burn` function:

```solidity
burn(0xStudentAddress, 50);
```

This will redeem 50 EduCoins from the student at `0xStudentAddress`.

## License

This project is licensed under the MIT License. 

## Author

Palak Singla





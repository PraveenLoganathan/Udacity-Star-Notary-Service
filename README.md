
**Project: Decentralized Star Notary Service**


This is the fifth project of the Udacity Blockchain Nanodegree. It is a decenteralized smart contract app that provides a web front end to create and lookup stars.
The DAPP implements the ERC-721 non-fungible token interface from openzeppelin and is deployed to the public Rinkeby Ethereum test network at the contract address:  
https://rinkeby.etherscan.io/address/0xE74a8d2f530719ea03d793c8231729C5CDEEAD11

1. ERC-721 Token Name: Star Token
2. ERC-721 Token Symbol: STX
3. Versions: Truffle v5.4.14 and OpenZeppelin 2.3.0

## Smart Contract Functions

The smart contract tokens have a name and a symbol in the StarNotary.sol file in the contracts folder.
Symbol is a short string "STX", which represents the Star Token Coin in this case.

The function `lookUptokenIdToStarInfo` in StarNotary.sol is implemented to look up stars using the token id. The function returns the name of the star.

```
function lookUptokenIdToStarInfo (uint _tokenId) public view returns (string memory) {}
```

A function called `exchangeStars` is added so two users can exchange their star tokens. This function does take the price into consideration, it is just used to exchange stars between users.

```
function exchangeStars(uint256 _tokenId1, uint256 _tokenId2) public {}
```

`transferStar` is used to transfer a star. The function transfers a star from the address of the caller and accepts two arguments. The first is the address to transfer the star to, and second argument is the token id of the star.

```
function transferStar(address _to1, uint256 _tokenId) public {}
```


## Supporting Unit Tests

Tests for the smart contract functions are written in the TestStarNotary.js file in the tests folder. Unit testing was done by leveraging the Mocha and Chai framework.

The following tests exist:

1. The token name and token symbol are added properly.
2. Users can exchange their stars.
3. Stars Tokens can be transferred from one address to another.

## Contract deployed to Rinkeby test network

The truffle-config.js file is setup to deploy the contract to the Rinkeby Public Network.
Infura is used in the truffle-config.js file for deployment to Rinkeby.

## Front end of the DAPP

When you click on the button "Look Up a Star" the application shows in the status the Star information.

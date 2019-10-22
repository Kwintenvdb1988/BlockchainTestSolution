# BlockchainTestSolution

This is a repository to save the solution for the test that can be found here:
https://github.com/argentlabs/application

1. Write a smart contract on the Ethereum blockchain. I used Remix for this:
http://remix.ethereum.org/
2. Enter personal email address in the “convertStringToKeccak” method. The result will be saved to the “hash” variable.
3. Use the get() method to retrieve the hash.
4. Use any proxy (I used MyEtherWallet) and send the hash to the apply() function in the contract defined in the test on the Ropsten network.
I made a test account for this and requested some free test eth. 
5. Retrieve your Id with the getApplicationID() method in the same contract. 
6. Bask in the glory of having completed your task and get a well deserved cappucino 

pragma solidity ^0.5.1;

contract test {
    
    bytes32 hash;
    
    function convertStringToKeccak ( string memory input) public returns (bytes32) {
        hash = keccak256(bytes(input));
    }

    function get() public view returns (bytes32) {
        return hash;
    }
}

hash result:
kwintenvdb@gmail.com
0x79587bef478da6b96c020476c6fc4d7718614f84746c8ed4dc9cfd2314bf49fd

public key test account
0xdb2f3792ccc34572eec9bc7207b4634d8f087530
private key test account
d94c3ae861dbf21494db02dbe22b1fc96930d2be2593c269e64b60eadc0b66ea

Transaction sending the keccak hash to the contract on Ropsten network
0x0dcea60432df9f056514d2112d592e56668031e359bd33d229a792363ce40f9e

solution of getApplicationId()
1559029141

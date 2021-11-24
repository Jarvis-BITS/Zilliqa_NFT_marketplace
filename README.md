# Zilliqa_NFT_marketplace

The contract works by accepting the wallet address of the owner of the non-fungible tokens and the buyer. The token count of buyer and owner is stored in a map. Once the buyer sends a request, the transfer of tokens can be undertaken after the owner has given permission. 

The contract takes input as owner i.e address of the contract owner, name and symbol of non-fungible token. It mainly consists of procedures and transitions
These transitions are invoked by sending a message to the contract. for eg when a message is sent to the contract (can be from the frontend through an API) asking for URI of an NFT the transition ``` GetnftURI ``` is executed along with the input parameter of the nft_id it has been given. 

1. Number of tokens and their id along with URI of owner's tokens are stored in mutable fields in the contract
2. A customer(buyer) obtains info of the owner's NFT's by invoking ```name(); symbol(); GetnftURI();``` 
3. Customer then tells owner what NFT's he wants to buy 
4. Owner invokes ``` Transfer() ``` to transfer his specified tokens to the customer. 
5. The transition checks if the addresses given are proper and changes the address of the NFT's owner to the customer then updates the token count accordingly

![image](https://user-images.githubusercontent.com/60312540/143194320-64dbd849-b014-4398-9c78-bce0514f0f03.png)

![image](https://user-images.githubusercontent.com/60312540/143194229-f8fdcac2-f093-4e74-a10f-256b01b30a02.png)


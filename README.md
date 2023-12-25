# NFT_smart_contract
The guide to create a NFT for a non-developer.


## Add the image/json metadata to the IPFS.
 The first steps is uploading both of your image and a json metadata to the IPFS. IPFS is created for storing those file as it will not be efficient to put them into the blockchain directly. Personally I am using [Pinata Cloud] (https://www.pinata.cloud/). It is free within a limited upload. You will first upload the image folder to Pinata and replace the URL link of the image into the template JSON file `metadata.json`. An example link will be: 
 > https://rose-junior-cardinal-547.mypinata.cloud/ipfs/{CID}/1.PNG
 And then upload the json file.
 You will find a CID of your uploaded JSON file. You can use it to identify your metadata in the IPFS. An example will be: 
 > https://ipfs.io/ipfs/{CID}/1.json

## Create and deploy the smart contract to the chain.
I 've given the template smart contract in this project. You can paste the compiled file into [Remix Ethereum] (https://remix.ethereum.org/) which is the tool we will deploy our smart contract into the chain. You will create a new file under the contract folder. Paste the compiled code into the new file. Make sure it is selected and click the solidity compiler from the left side tool bar. Once the code is compiled, go to deploy and run transactions. Chose the injected provider as yor environment. Connect your wallet to the website. You can verify it by checking whether the account and balance are correctly loaded.  Select the your smart contract and click deploy. Then your contract will be on the chain.

## Mint your NFT.
Once your smart contract is deployed, you will see all the methods in the contract. Find the mint function and paste your address of the ipfs json file in it and click call. Then your NFT is created! You can find it on the [opensea](https://opensea.io/) by searching on your address. 



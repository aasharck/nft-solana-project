
# NFT Minting With Solana

## Running the DApp
1. clone this repo
2. ``` cd client ```
3. ``` yarn install ```
4. ``` yarn start ```


## How to Create the Same

### Setting up sugar

1. To install Sugar


```
 <(curl -sSf https://sugar.metaplex.com/install.sh)
```
2. Install Solana CLI tool
```
sh -c "$(curl -sSfL https://release.solana.com/v1.10.32/install)"
```
3. Ensure both are installed
```
sugar --version
solana --version
```
4. Set up a wallet
```
solana-keygen new --outfile ./wallets/owner.json
```
5. Set keypair
```
solana config set --keypair /home/aashar/sol-projects/nftproject/wallets/owner.json
```
6. Change to devnet
```
solana config set --url https://api.devnet.solana.com
```
7. Get some test SOL for testing
```
solana airdrop 2
```
8. Once you have the above set up, You can now create the assets(images + json for NFT). For this example, I will be using the [sample assets from Metaplex](https://docs.metaplex.com/assets/files/assets-ff6bd873ecd07b49c86faf3c7aab82d2.zip).

9. Download and unzip it in your project folder

10. use the command below to run the candy machine cli (sugar)
```
sugar launch
```
This will launch an simple command line app which will ask you a bunch of questions:

![App Screenshot](https://gcdnb.pbrd.co/images/itD4SY4EYbFG.png?o=1)

Once it's done, candy machine will be deployed and you can see it on [Solscan](https://solscan.io/account/2wmRaA99qUxCxVegqz75MtMTgbM7x3UmVW4g4q53MFVo?cluster=devnet)
Please save the candy machine id from the terminal

### Frontend Setup

1. For the frontend we will actually use a boilerplate code given to us by metaplex. You can clone the repo by executing the command below:
```
git clone https://github.com/metaplex-foundation/candy-machine-ui ./client
```
2. Then get inside the client dir and execute:
```
yarn install
```
3. rename the .env.example to .env and change the candy machine ID to the one you saved before. Also change the RPC host url to https://api.devnet.solana.com

4. then finally run the below command
```
yarn start
```

The Dapp will open up and you will be able to mint some nfts to your wallet.
Make sure you have Phantom wallet installed. Also you will be able to find the minted nfts from your wallet itself.
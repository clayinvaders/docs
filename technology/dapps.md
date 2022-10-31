# dApps

### Intro

dApps and Wallets are today the tip of the iceberg for the new WEB3.0.

dApp is an app that connects some interfase (web/mobile/app) to a decentralized environment and are free from control and interference by any single authority.

The most common way to be connected to a dApp, is thought the use of a wallet.

### CIP-0030 Standard&#x20;

The standard describes a webpage-based communication bridge allowing webpages (i.e. dApps) to interface with Cardano wallets.

{% embed url="https://github.com/cardano-foundation/CIPs/blob/master/CIP-0025/README.md" %}

### How it Works?

A extension wallet injects the api in the browser page, this creates a bridge that connects the page to the wallet features & the blockchain.

### Connect

* Call cardano.{walletName}.isEnabled(): Promise \<bool>
  * Returns&#x20;
  * If false, will ask the user to connect the dApp with the wallet
* Call cardano.{walletName}.enable(): Promise \<API>
  * This returns the **api 🛸**
* Use the **api**

### Full Api

Here a description of more used functions of the api.

cardano.{walletName}

* icon
* name
* isEnabled(): returns true if the dApp is already connected to the user's wallet
* enable(): returns the api instance

api

* getNetworkId(): 1 is Mainnet
* getUtxos(): returns list of UTxOs
* getCollateral(): returns list of Collateral UTxOs
* getBalance(): returns the summing of getUtxos()
* getUsedAddresses(): returns the list of all used addresses (included in some on-chain transaction)
  * Some wallets (Nami) have Single Address Model (SAM) by default
  * If wallet is working as SAM, it returns only 1 Address
* getRewardAddresses(): returns the list reward (stake) address.
  * Is possible to have more than 1 (CIP-0018)
  * In practice 99%+ it returns only 1
* signTx(): ask for a sign of the \`transaction\` in the extension, and returns the witness&#x20;
  * If partialSign para is true, the wallet only tries to sign what it can (This is how multisig transactions works)
* signData(): ask for a sign of the \`payload\` in the extension.&#x20;
  * &#x20;Follows [CIP-0008](https://github.com/cardano-foundation/CIPs/blob/master/CIP-0008/CIP-0008.md)
* submitTx(): returns the transaction id for the dApp to track


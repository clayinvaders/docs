---
description: Extended Unspent Transactions Outputs
---

# EUTxOs

Understanding of how the UTxOs works is mandatory to build an a scalable dApp in Cardano.

There is a lot of articles explaining how eUTxOs works, but there is no much content explaining what are the practices to use them for MINTING in a Mutisig, or how to deal with them for a CLAIMING system.

Is a #CNFTCommunity creators to help everyone understand how to deal with it.

### **Balance**

When you create a TX, you need to ensure that Input and Output are balanced.

There are three types of operations for tokens:&#x20;

* Send Token Transaction&#x20;
  * Inputs  = outputs + fee
    * Input =&#x20;
      * ADDRESS 1 => 100 ADA + **1** **ClayInvader#00123**
    * Output =
      * ADDRESS 2 => 49.7 ADA
      * ADDRESS 2 => 50 ADA + **1** **ClayInvader#00123**
    * Fee =
      * 0.3 ADA
* Mint Token Transaction
  * Inputs = outputs + fee - mint
    * Input =&#x20;
      * ADDRESS 1 => 100 ADA
    * Output =
      * ADDRESS 2 => 49.7 ADA
      * ADDRESS 2 => 50 ADA + **1 ClayInvader#12345**
    * Fee =
      * 0.3 ADA
    * Mint
      * 1 **ClayInvader#12345**
* Burn Token Transaction
  * Inputs = outputs + fee + burn
    * Input =&#x20;
      * ADDRESS 1 => 100 ADA + **1 ClayInvader#54321**
    * Output =
      * ADDRESS 2 => 100 ADA&#x20;
    * Fee =
      * 0.3 ADA
    * Burn
      * 1 **ClayInvader#54321**

### UTxO Selection

There are many strategies to select UTxOs, most of them are focused on selecting the best UTxOs that fit the amount of ADA + Tokens required, but none of them resolves the Parallelization, Tx Size Limits and the min ADA required for each output.

### Parallelization

The biggest complexity in a CNFT project is to manage the EUTxOs in a proper to allow more than 1 person play with it at a time, if it's not well managed, you could see the well known UTXOS\_EXHAUSTED 😂

### Tx Size Limit

The limit is 16KB for a tx, that means if you have to send 100+ tokens, you will have an important reduction of the size you could use for the minting metadata.

### Min ADA & Fee

Each output must have a min amount of ADA, and you need to consider the fee as well in the balance of inputs and outputs when you create Tx.

ie.&#x20;

* Inputs  = outputs + fee
  * Input =&#x20;
    * ADDRESS 1 (buyer)
      * Utxo =>  20 ADA&#x20;
      * Utxo =>  31 ADA (51 in total, but not covering fee + minADA)
      * Utxo =>  10 ADA (needed)
  * Output =
    * ADDRESS 2 => 50 ADA
    * ADDRESS 1 => 10.7 ADA + **1** **ClayInvader#00123**
  * Fee =
    * 0.3 ADA

The mint cost is 50 ADA, but you need to cover also the return of the output with the token to yourself.

Sometimes this is not analyzed during the UTxO selection and some "random" transactions fail.&#x20;

If you want to go deeper, check this [https://github.com/input-output-hk/cardano-ledger/blob/master/doc/explanations/min-utxo-alonzo.rst](https://github.com/input-output-hk/cardano-ledger/blob/master/doc/explanations/min-utxo-alonzo.rst)&#x20;

### Minter Machine (Use Case)

It's not rare to see 1 UTxO with many tokens (+100) inside a wallet of a CNFT collector, and that makes it harder to process.

There many decisions to take in the selection of UTxOs, but usually the most simple and effective way to do it is filtering UTxOs with many tokens and inform properly if you don't find enough ADA to cover the cost of the NFT + fees + minADA.

Remember that selecting many UTxOs could carry with a big count of tokens.

### Claimer Machine (Use Case)

One common case for a Claiming Machines is that you have a wallet where the token you want to distribute resides.&#x20;

To allow more than 1 person claim at the same time, you need to make an advance management of the UTxOs. If not, you need to wait until 1 tx is finished to start the following or be ready to receive a bunch of UTXOS\_EXHAUSTED

We divide this in 3 stages:

* Split:&#x20;
  * You need at least 1 UTxOs to covers the amount needed, for each claimer in parallel.
  * You can trigger the split based on the amount of unused UTxOs
* Use:
  * You need to track each used UTxO, to not reuse the same more than once
* Refresh:
  * You need to refresh the list of unused UTxOs periodically to ensure the sync with the blockchain

### More

If you want to see a advance article about eUTxOs and the differences between them and the Accounting model [https://medium.com/coinmonks/understanding-cardano-extended-utxo-950ae19829cf](https://medium.com/coinmonks/understanding-cardano-extended-utxo-950ae19829cf)




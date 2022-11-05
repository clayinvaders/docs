# NFT Storage

### Filetypes

There is no limitation of types, but to follow the standard for NFTs (CIP-0025) you need to have at least 1 image (jpg/png/gif). This is usually the one you will see as a thumb in sites like jpg.store or pool.pm.\
\
[https://github.com/cardano-foundation/CIPs/blob/master/CIP-0025/README.md](https://github.com/cardano-foundation/CIPs/blob/master/CIP-0025/README.md)

### On-Chain vs Off-Chain

In Cardano, the biggest size of 1 single transaction is 16KB, so that means that you need to keep some space for the rest of the information that the transaction needs to be executed.

A rule could be, If the size in bytes of the pieces of art you generate is > 12K, you need to go storage off-chain. We will go deeper into the UTxOs explanation.

### On-Chain

All the metadata for the NFT is stored in the transaction in the NFT is minted in.&#x20;

That means the NFT will always live as long as the blockchain is stored on lives!

Pros:

* Will be there forever! 🙏

Cons:

* You are super limited with the type of art you can create

### Off-Chain / IPFS

If you talk about Off-Chain storage, you talk about IPFS (InterPlanetary File System).

IPFS is a distributed system for storing and accessing files.

Project using IPFS the image is not stored in the blockchain, a hash reference to the image is stored instead.

There are many IPFS providers (NFT.Storage, Pinata, Blockfrost)

Pros:&#x20;

* You have no limitations on your collection. Your creativity is the limit.

Cons:&#x20;

* You need to pay to pin images (There are free services like NFT.Storage but with limitations)
* Improvable, but IPFS could not be online or a standard in the future&#x20;

### Upload

When you have a 10K collection, probably you are talking about 10\~20 Gigas of data or more to upload.&#x20;

In Clay Invaders, we use a lib to upload them that works like a charm (we are using Pinata)\
[https://github.com/clayinvaders/pinata-ipfs-scripts-for-nft-projects](https://github.com/clayinvaders/pinata-ipfs-scripts-for-nft-projects)

Once you upload all your files, you need to replace all the metadata files with the new ipfs hashes (Thumb and full size).\
\
This is the code we use for it:

{% embed url="https://gist.github.com/clayinvaders/b8640b6426d78ca9f3a62e6c1fb5e187" %}
replace\_ipfs\_hashes.js
{% endembed %}

So if you have the art generated but don't know how to upload them to IPFS, take a look and feel free to ping us!&#x20;


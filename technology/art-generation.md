# Art Generation

One of the most common ways to generate a collection is to work in traits and assemble them algorithmically.

You don't need to create a tool from scratch to do this, here we share the changes we did to a great lib called **Hashlips Art Generation Lib**.

We adapted it to:

* Cardano Metadata
* Simplified Configuration&#x20;

[https://github.com/clayinvaders/cardano-hashlips\_art\_engine](https://t.co/JiVX9Vuala)

So if you have the traits but don't know how to assemble them, take a look and feel free to ping us!

### Thumbs

Part of the Standard for NFTs in Cardano asks you to have a thumb image of your NFT in the metadata. (400x400 or 500x500) could be a good size for them.

We strongly suggest you use [**ImageMagick**](https://github.com/ImageMagick/ImageMagick)**,** with a simple script as follows you could convert them in minutes. :fire:

{% embed url="https://gist.github.com/clayinvaders/a9332ace06eef7f2207f79d58320419b" %}
convert\_images.sh
{% endembed %}

So if you have the images but don't know how to generate the thumbs, take a look and feel free to ping us!

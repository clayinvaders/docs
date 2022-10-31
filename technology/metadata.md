# Metadata

### The Standard

CIP-0025 is today the standard for NFTs

{% embed url="https://github.com/cardano-foundation/CIPs/blob/master/CIP-0025/README.md" %}

### Metadata

The metadata is a JSON where we define each NFT.

```json
{
  "721": {
    "<policy_id>": {
      "<asset_name>": {
        "name": <string>,

        "image": <uri | array>,
        "mediaType": image/<mime_sub_type>,

        "description": <string | array>,

        "files": [{
          "name": <string>,
          "mediaType": <mime_type>,
          "src": <uri | array>,
          <other_properties>
        }],

        <other properties>
      }
    },
    "version": <version_id>
  }
}
```

The required fields are:

```json
{
  "721": {
    "<policy_id>": {
      "<asset_name>": {
        "name": <string>,
        "image": <uri | array>,
      }
    }
  }
}
```

Where

* 721: The tag "721"  indicate this is NFT
  * \<policy\_id>: The id of the policy generated based on expiration and the hash of the public keys.
    * \<asset\_name>: The name you want to give the asset, no special characters nor spaces

Note: 721, is inherit from [https://eips.ethereum.org/EIPS/eip-721](https://eips.ethereum.org/EIPS/eip-721)

### Clay Invaders Metadata

```json
{
  "721": {
    "32c4d39b4db9bfea17b92159e9e29b30888a8a72b5e14ec00c5d2b27": {
      "ClayInvaders02486": {
        "name": "ClayInvaders #02486",
        "description": [
          "ClayInvaders invading galaxies and #Cardano with their",
          " magical, mysterious and clumsy ways."
        ],
        "image": "ipfs://QmdvnVLYBqjsq5NZrcY58PLfAdocy7AzCftkY3LQZPxbrk",
        "files": [
          {
            "mediaType": "image/png",
            "src": "ipfs://Qman36W8yJ4itjfp1m43vssmRNfoMtnLHetQLbXEA3EJNs"
          }
        ],
        "mediaType": "image/png",
        "Attributes": {
          "Galaxy": "Condor 1",
          "Spaceship": "None",
          "Planets": "One",
          "Pet": "None",
          "Horns": "Pink Neon 1",
          "Eyes": "Two: Green",
          "Brows": "White Cut",
          "Mouth": "Smile Arrow",
          "Bandages_Head": "None",
          "Accessories": "None",
          "Suit": "Doctor"
        },
        "Publisher": "www.clayinvaders.art",
        "Twitter": "@clayinvaders",
        "Type": "Crew"
      }
    }
  }
}
```

Notes:

* Top level image is the image that is used as thumb in external sites like pool.pm or jpg.store
* The Image inside files, is the full size (2000x2000)
* Type: We define each NFT as Spaceship, Crew or Passenger
* Describing all traits inside Attributes tag, it's not an standard, but a good practice

### New CIP

(we suppose this section will be updated soon)

There is a new standard in discussion (proposed by Alessandro/Berry, as usual 😂 ) but not so many projects using it yet.&#x20;

[https://github.com/cardano-foundation/CIPs/tree/master/CIP-0067](https://github.com/cardano-foundation/CIPs/tree/master/CIP-0067)

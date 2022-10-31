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

Mandatory&#x20;

* 721: The tag "721"  indicate this is NFT
  * \<policy\_id>:&#x20;

### Notes

There is a new standard in discussion (proposed by Alessandro/Berry, as usual 😂 ) but not to many projects using it yet.&#x20;

[https://github.com/cardano-foundation/CIPs/tree/master/CIP-0067](https://github.com/cardano-foundation/CIPs/tree/master/CIP-0067)

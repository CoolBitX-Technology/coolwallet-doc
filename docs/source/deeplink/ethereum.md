# Ethereum

* coinType: ETH

**DeepLink URI**

```
coolwallet://ETH/{action}?param=
```


## Supported Actions

### getAccounts


- Parameters :
  - ( no parameters )


- Example :
```
coolwallet://ETH/getAccounts/
```

- Return data : Array of Address
```
["0x8c03377931f3ca36154399c5516370bc6d54e81e"]
```

### signMessage

- Parameters :
  - from : Address
  - data : Signing Data
  - raw ( Optional ) : If data is hashed, this is the raw data for advanced verification


- Example :
```
coolwallet://ETH/signMessage?from=0xbAF99eD5b5663329FA417953007AFCC60f06F781&data=0xbbf0ab1e9bd8cff92628e7fa4a6044985df9399c8d3c7de6897d980b3e312734&raw=0x04f062809b244e37e7fdc21d9409469c989c234200000000000000000000000000000000000000000000000000000000000f42400000000000000000000000000000000000000000000000000000b5e620f48000000000000000000000000000000000000000000000000000000000000005b8d85b50643f000a000500007d00dde12a12a6f67156e0da672be05c374e1b0a3e57
```

- Return data : Signature
```
"0x50d7441ad2e08c07cf296ea4bddee7c6930a0e593bb5a4cacd1901cb902f61787e28cfd4e112d0f944e107c066118e52999525cb964a2e6648fc399dadd3de901b"
```

### signTypedData

- Parameters :
  - from : Address
  - data : TypedData with stringified JSON format


- Example :
```
coolwallet://ETH/signTypedData?from=0xbAF99eD5b5663329FA417953007AFCC60f06F781&data={"types":{"EIP712Domain":[{"name":"name","type":"string"},{"name":"version","type":"string"},{"name":"chainId","type":"uint256"},{"name":"verifyingContract","type":"address"}],"Person":[{"name":"name","type":"string"},{"name":"wallet","type":"address"}],"Mail":[{"name":"from","type":"Person"},{"name":"to","type":"Person"},{"name":"contents","type":"string"}]},"primaryType":"Mail","domain":{"name":"Ether Mail","version":"1","chainId":1,"verifyingContract":"0xCcCCccccCCCCcCCCCCCcCcCccCcCCCcCcccccccC"},"message":{"from":{"name":"Cow","wallet":"0xCD2a3d9F938E13CD947Ec05AbC7FE734Df8DD826"},"to":{"name":"Bob","wallet":"0xbBbBBBBbbBBBbbbBbbBbbbbBBbBbbbbBbBbbBBbB"},"contents":"Hello, Bob!"}}
```

- Return data : Signature
```
"0x4355c47d63924e8a72e509b65029052eb6c299d53a04e167c5775fd466751c9d07299936d304c153f6443dfa05f40ff007d72911b6f72307f996231605b915621c"
```

### signTransaction


- Parameters :
  - from : Address
  - to: Address
  - value: Hex String
  - gas: Hex String
  - gasPrice: Hex String
  - nonce: Hex String
  - data: Hex String


- Example :
```
coolwallet://ETH/signTransaction?from=0x8c03377931f3ca36154399c5516370bc6d54e81e&to=0x7037734b180c44b7041a31666486f81f45860541&value=0xde0b6b3a7640000&gas=0x5208&gasPrice=0xee6b2800&nonce=0x141&data=0x1234
```

- Return data : Signed Transaction
```
"0xf86e827f738509502f900082c350947b0db0f1af5920977746c632d107b302b5d669da880354c86135f350008026a0f57dd7cc619adbb3fd57e07063b970d5bba48205baf073dbe67fa32c3ecc06bda079b8ce6d8c59d53ab3e6d081ce48c348593a18e2fc9993e72b4e2023c4c4355e"
```

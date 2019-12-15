# Bitcoin

* coinType: BTC

**DeepLink URI**

```
coolwallet://ETH/{action}?param=
```

## Supported Actions

### signP2WPKH

#### Parameters

| name | type | Notes |
| -------- | -------- | -------- |
| inputs     | input[]     | Array of [utxo input](#input)s |
| outputs     | output[2]     | Array of [utxo output](#output)s. You must provide exactly **2** outputs in the following order: [{Target Output}, {Change Output}]     |
| changeAddressIndex | number     ||

* Returns: (hex) signed message.

#### Example Url

```url
coolwallet://BTC/signP2PKH?inputs=[{"txId":"3735fd3e4618295e62f74d2cd4c9d34a20c2f4f5ad97ee206e1c79c4f01be5ca","vout":2,"value":97184,"redeemScript":"00148a99a17ee968fb47e3a446a24a49bed1f872808b","addressIndex":2}]?outputs=[{"address":"3KvJ1uHPShhEAWyqsBEzhfXyeh1TXKAd7D""value":10000},{"value":80710,"address":"3NwVRNJegGwJdgYbAZs35CYttLYz2rE7bg"}]?changeAddressIndex=2
```

## Cutom Types

### Input

```
{
    txId: string,
    vout: number,  
    value: number,
    addressIndex: number,
    redeemScript: string, (optional - required when signing P2WPKH)
}

```

### Output

```
{
    address: string,
    value: number
}
```

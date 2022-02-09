# `contract-call-decoder`

## Overview

Fetches the metadata file from IPFS/Swarm functionality to the contract call decoder
Fetches the contract's deployedByteCode functionality to contract call decoder
Decodes function name and params from tx input and match via ABI + userdoc

> see https://github.com/ethereum/sourcify/issues/538

## Usage

The module can be a class that takes two parameters in constructor: an RPC and an optional IPFS/Swarm Gateway (can default to ipfs.io/ipfs/ and swarm-gateways.net).


```ts 
import Decoder from 'contract-call-decoder'

const decoder = new Decoder('https://rinkeby.infura.io/v3/<Access-Token>', { ipfs: 'https://ipfs.infura.io/ipfs/' })
const decodedTx = decoder.decodeContractCall('0x40c10f19000000000000000000000000aa6042aa65eb93c6439cdaebc27b3bd09c5dfe940000000000000000000000000000000000000000000000000de0b6b3a7640000', '0x7492F518e41D8610a677Fe84b39223b746449979')
```


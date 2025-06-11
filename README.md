# Synthra Swap Router

This repository contains smart contracts for swapping on the Synthra V3 protocols.

## Local deployment

In order to deploy this code to a local testnet, you should install the npm package
`@synthra-swap/swap-router-contracts`
and import bytecode imported from artifacts located at
`@synthra-swap/swap-router-contracts/artifacts/contracts/*/*.json`.
For example:

```typescript
import {
  abi as SWAP_ROUTER_ABI,
  bytecode as SWAP_ROUTER_BYTECODE,
} from '@synthra-swap/swap-router-contracts/artifacts/contracts/SwapRouter02.sol/SwapRouter02.json'

// deploy the bytecode
```

This will ensure that you are testing against the same bytecode that is deployed to
mainnet and public testnets, and all Synthra code will correctly interoperate with
your local deployment.

## Using solidity interfaces

The swap router contract interfaces are available for import into solidity smart contracts
via the npm artifact `@synthra-swap/swap-router-contracts`, e.g.:

```solidity
import '@synthra-swap/swap-router-contracts/contracts/interfaces/ISwapRouter02.sol';

contract MyContract {
  ISwapRouter02 router;

  function doSomethingWithSwapRouter() {
    // router.exactInput(...);
  }
}

```

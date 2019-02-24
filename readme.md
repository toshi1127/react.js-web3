# react.js-web3

- By detecting login and logout of MetaMask, you can develop high DApps of UX.
- Supports import of contracts

## Installation

`npm install --save react.js-web3`

## Usage
### Web3Container
```
import { Web3Container } from 'react.js-web3'

// ...

render () {
  return (
    <Web3Container
      renderLoading={() => <div>Loading Accounts Page...</div>}
      render={({ accounts }) => <Examples accounts={accounts} />}
    />
  )
}
```

- renderLoading 
You can specify the View that is displayed when web3.js can not acquire account.
- render
You can pass the account as props to the React Component.

### getContract

```
import { getWeb3, getContract } from "react.js-web3";
import contractDefinition from '@contracts/SimpleStorage.json'

// ...

const web3 = await getWeb3();
const contract = await getContract(web3, contractDefinition)
```

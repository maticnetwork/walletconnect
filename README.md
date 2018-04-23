# WalletConnect

Simple library to connect with wallet-connect's bridge server. Works with browsers, node.js and react-native.

You can read more about WalletConnect protocol here: http://walletconnect.org/

## install

```bash
npm install --save walletconnect # yarn add walletconnect
```

## Example

```js
import {generateKey, WalletConnector} from 'walletconnect'

// create shared key
const sharedKey = await generateKey()

// create wallet connector
const walletConnector = new WalletConnector(
  'https://walletconnect.matic.network',
  sharedKey
)

// data
const data = {address: '0x0'}

// encrypted object
const encryptedObj = await walletConnector.encrypt(data)

// decrypted data
const decrypted = walletConnector.decrypt(obj).data
```

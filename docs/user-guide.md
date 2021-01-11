# User Guide

All information for developers using `vapjs-rpc` should consult this document.

## Install

```
npm install --save vapjs-rpc
```

## Usage

```js
const HttpProvider = require('vapjs-provider-http');
const VapRPC = require('vapjs-rpc');
const vap = new VapRPC(new HttpProvider('http://localhost:8545'));

vap.sendAsync({ method: 'vap_accounts' }, (err, accounts1) => {
  // null ['0x...', '0x....']
});

vap.sendAsync({ method: 'vap_gasPrice' }, (err, gasPrice) => {
  // null '0xe83922'
});
```

## Async Only

All methods are `async` only.

## Error handling

Error handling is done through function callbacks or promised catches.

## Supported Methods

`vapjs-rpc` supports all Vapory spec RPC methods.

* [vap_protocolVersion](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_protocolversion)
* [vap_syncing](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_syncing)
* [vap_coinbase](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_coinbase)
* [vap_mining](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_mining)
* [vap_hashrate](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_hashrate)
* [vap_gasPrice](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_gasprice)
* [vap_accounts](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_accounts)
* [vap_blockNumber](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_blocknumber)
* [vap_getBalance](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_getbalance)
* [vap_getStorageAt](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_getstorageat)
* [vap_getTransactionCount](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_gettransactioncount)
* [vap_getBlockTransactionCountByHash](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_getblocktransactioncountbyhash)
* [vap_getBlockTransactionCountByNumber](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_getblocktransactioncountbynumber)
* [vap_getUncleCountByBlockHash](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_getunclecountbyblockhash)
* [vap_getUncleCountByBlockNumber](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_getunclecountbyblocknumber)
* [vap_getCode](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_getcode)
* [vap_sign](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_sign)
* [vap_sendTransaction](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_sendtransaction)
* [vap_sendRawTransaction](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_sendrawtransaction)
* [vap_call](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_call)
* [vap_estimateGas](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_estimategas)
* [vap_getBlockByHash](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_getblockbyhash)
* [vap_getBlockByNumber](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_getblockbynumber)
* [vap_getTransactionByHash](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_gettransactionbyhash)
* [vap_getTransactionByBlockHashAndIndex](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_gettransactionbyblockhashandindex)
* [vap_getTransactionByBlockNumberAndIndex](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_gettransactionbyblocknumberandindex)
* [vap_getTransactionReceipt](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_gettransactionreceipt)
* [vap_getUncleByBlockHashAndIndex](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_getunclebyblockhashandindex)
* [vap_getUncleByBlockNumberAndIndex](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_getunclebyblocknumberandindex)
* [vap_getCompilers](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_getcompilers)
* [vap_compileLLL](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_compilelll)
* [vap_compileSolidity](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_compilesolidity)
* [vap_compileSerpent](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_compileserpent)
* [vap_newFilter](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_newfilter)
* [vap_newBlockFilter](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_newblockfilter)
* [vap_newPendingTransactionFilter](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_newpendingtransactionfilter)
* [vap_uninstallFilter](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_uninstallfilter)
* [vap_getFilterChanges](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_getfilterchanges)
* [vap_getFilterLogs](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_getfilterlogs)
* [vap_getLogs](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_getlogs)
* [vap_getWork](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_getwork)
* [vap_submitWork](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_submitwork)
* [vap_submitHashrate](https://github.com/vaporyco/wiki/wiki/JSON-RPC#vap_submithashrate)

* [web3_clientVersion](https://github.com/vaporyco/wiki/wiki/JSON-RPC#web3_clientversion)
* [web3_sha3](https://github.com/vaporyco/wiki/wiki/JSON-RPC#web3_sha3)

* [net_version](https://github.com/vaporyco/wiki/wiki/JSON-RPC#net_version)
* [net_peerCount](https://github.com/vaporyco/wiki/wiki/JSON-RPC#net_peercount)
* [net_listening](https://github.com/vaporyco/wiki/wiki/JSON-RPC#net_listening)

* [db_putString](https://github.com/vaporyco/wiki/wiki/JSON-RPC#db_putstring)
* [db_getString](https://github.com/vaporyco/wiki/wiki/JSON-RPC#db_getstring)
* [db_putHex](https://github.com/vaporyco/wiki/wiki/JSON-RPC#db_puthex)
* [db_getHex](https://github.com/vaporyco/wiki/wiki/JSON-RPC#db_gethex)

* [shh_post](https://github.com/vaporyco/wiki/wiki/JSON-RPC#shh_post)
* [shh_version](https://github.com/vaporyco/wiki/wiki/JSON-RPC#shh_version)
* [shh_newIdentity](https://github.com/vaporyco/wiki/wiki/JSON-RPC#shh_newidentity)
* [shh_hasIdentity](https://github.com/vaporyco/wiki/wiki/JSON-RPC#shh_hasidentity)
* [shh_newGroup](https://github.com/vaporyco/wiki/wiki/JSON-RPC#shh_newgroup)
* [shh_addToGroup](https://github.com/vaporyco/wiki/wiki/JSON-RPC#shh_addtogroup)
* [shh_newFilter](https://github.com/vaporyco/wiki/wiki/JSON-RPC#shh_newfilter)
* [shh_uninstallFilter](https://github.com/vaporyco/wiki/wiki/JSON-RPC#shh_uninstallfilter)
* [shh_getFilterChanges](https://github.com/vaporyco/wiki/wiki/JSON-RPC#shh_getfilterchanges)
* [shh_getMessages](https://github.com/vaporyco/wiki/wiki/JSON-RPC#shh_getmessages)


## Browser Builds

`vapjs` provides production distributions for all of its modules that are ready for use in the browser right away. Simply include either `dist/vapjs-rpc.js` or `dist/vapjs-rpc.min.js` directly into an HTML file to start using this module. Note, an `VapRPC` object is made available globally.

```html
<script type="text/javascript" src="vapjs-rpc.min.js"></script>
<script type="text/javascript">
new VapRPC(...);
</script>
```

Note, even though `vapjs` should have transformed and polyfilled most of the requirements to run this module across most modern browsers. You may want to look at an additional polyfill for extra support.

Use a polyfill service such as `Polyfill.io` to ensure complete cross-browser support:
https://polyfill.io/

## Latest Webpack Figures

```
Version: webpack 2.1.0-beta.15
Time: 859ms
             Asset    Size  Chunks             Chunk Names
    vapjs-rpc.js  175 kB       0  [emitted]  main
vapjs-rpc.js.map  219 kB       0  [emitted]  main
   [4] ./lib/index.js 5.02 kB {0} [built]
    + 13 hidden modules

Version: webpack 2.1.0-beta.15
Time: 2699ms
             Asset     Size  Chunks             Chunk Names
vapjs-rpc.min.js  78.5 kB       0  [emitted]  main
   [4] ./lib/index.js 5.02 kB {0} [built]
    + 13 hidden modules
```

## Other Awesome Modules, Tools and Frameworks

### Foundation
 - [web3.js](https://github.com/vaporyco/web3.js) -- the original Vapory JS swiss army knife **Vapory Foundation**
 - [vaporyjs](https://github.com/vaporycojs) -- critical vapory javascript infrastructure **Vapory Foundation**
 - [browser-solidity](https://vapory.github.io/browser-solidity) -- an in browser Solidity IDE **Vapory Foundation**

### Nodes
  - [geth](https://github.com/vaporyco/go-vapory) Go-Vapory
  - [parity](https://github.com/ethcore/parity) Rust-Vapory build in Rust
  - [testrpc](https://github.com/vaporycojs/testrpc) Testing Node (vaporyjs-vm)

### Testing
 - [wafr](https://github.com/silentcicero/wafr) -- a super simple Solidity testing framework
 - [truffle](https://github.com/ConsenSys/truffle) -- a solidity/js dApp framework
 - [embark](https://github.com/iurimatias/embark-framework) -- a solidity/js dApp framework
 - [dapple](https://github.com/nexusdev/dapple) -- a solidity dApp framework
 - [chaitherium](https://github.com/SafeMarket/chaithereum) -- a JS web3 unit testing framework
 - [contest](https://github.com/DigixGlobal/contest) -- a JS testing framework for contracts

### Wallets
 - [ethers-wallet](https://github.com/ethers-io/ethers-wallet) -- an amazingly small Vapory wallet
 - [metamask](https://metamask.io/) -- turns your browser into an Vapory enabled browser =D

## Our Relationship with Vapory & VaporyJS

 We would like to mention that we are not in any way affiliated with the Vapory Foundation or `vaporyjs`. However, we love the work they do and work with them often to make Vapory great! Our aim is to support the Vapory ecosystem with a policy of diversity, modularity, simplicity, transparency, clarity, optimization and extensibility.

 Many of our modules use code from `web3.js` and the `vaporyjs-` repositories. We thank the authors where we can in the relevant repositories. We use their code carefully, and make sure all test coverage is ported over and where possible, expanded on.


# Ethereum Rpc .NET

**C# .NET wrapper for Ethereum RPC client**
## Thanks to NEthereum and other sample .Net implementations

Notes: ssh protocol is partially implemented and db_putString, db_getString, db_putHex, db_getHex have been deprecitated

Supported objects
--------

- Address
- Block
- Filter
- Log
- Whisper
- Work

Supported RPC calls
--------

- web3_clientVersion
- web3_sha3
- net_version
- net_peerCount
- net_listening
- eth_protocolVersion
- eth_syncing
- eth_coinbase
- eth_mining
- eth_hashrate
- eth_gasPrice
- eth_accounts
- eth_blockNumber
- eth_getBalance
- eth_getStorageAt
- eth_getTransactionCount
- eth_getBlockTransactionCountByHash
- eth_getBlockTransactionCountByNumber
- eth_getUncleCountByBlockHash
- eth_getUncleCountByBlockNumber
- eth_getCode
- eth_sign
- eth_sendTransaction
- eth_sendRawTransaction
- eth_call
- eth_estimateGas
- eth_getBlockByHash
- eth_getBlockByNumber
- eth_getTransactionByHash
- eth_getTransactionByBlockHashAndIndex
- eth_getTransactionByBlockNumberAndIndex
- eth_getTransactionReceipt
- eth_getUncleByBlockHashAndIndex - **untested**
- eth_getUncleByBlockNumberAndIndex - **untested**
- eth_getCompilers
- eth_compileLLL
- eth_compileSolidity
- eth_compileSerpent
- eth_newFilter
- eth_newBlockFilter
- eth_newPendingTransactionFilter
- eth_uninstallFilter
- eth_getFilterChanges
- eth_getFilterLogs
- eth_getLogs
- eth_getWork
- eth_submitWork
- eth_submitHashrate
- shh_version

Configuration
-------------

	<?xml version="1.0" encoding="utf-8"?>
	<configuration>
	
		<appSettings>
			<add key="EthereumRpcUrl" value="http://localhost"/>
			<add key="EthereumRpcPort" value="8545"/>
		</appSettings>
				
	</configuration>
	
	
Getting started
--------

	var connectionOptions = new ConnectionOptions()
	{
		Port = "8545",
		Url = "http://localhost"
	};
	
	var ethereumService = new Web3Mobile(connectionOptions);

Roadmap
--------

- All RPC calls implemented
- Address Parser
- Hash functions
- Helpers for non ethereum types

## Sample Output
`
94006729117558243750

0x2c354b77ca94c43d24c9fb67c34fa1c1dd71646052babe8647199ca9ed43537c

0x058e8f70bca15aa86857cb9d2ee4c02724d157940b3d71af90d1a831d642dbea

EthereumJS TestRPC/v2.13.1/ethereum-js

0xed6c11b0b5b808960df26f5bfc471d04c1995b0ffd2055925ad1be28d6baadfd

5777

True

63

StartingBlock:

CurrentBlock:

HighestBlock:

IsSyncing:False

0xb884ff4b46c7d0ccb68d280ef39b3cbe8fd47590

True

0

20000000000

[0xb884ff4b46c7d0ccb68d280ef39b3cbe8fd47590] [0x7b953144da42fe99d15411ae9e945c877b1b839c] [0x9ea4c939ba86216cd668720fab229957d47cb98c] [0xf933ece5132655d98cd3e5d64bd442fefc65abe2] [0x602337414982f13c01ed0585472e45e2619e292a] [0x640aef81f42299ad958aac7b4e9f76247071abb1] [0xd6af3e021f835c8d324a31d366e82ecdeaaade42] [0xe8a15d86e739fb60f81ade5fb4fc66b61cf4a0f9] [0x7ac91b385ec863427c4c1202086f75f359c5024b] [0x19f914e69cd70c9407f6e0f4470c536a176ea016] account :94

sign : 0x501d8d6acda72ff16237b5810f412de68aa3090e8f9492fb69e1a5471108282a6a14da16d6f7332ec006fb86368ff2f80bf28547f9c53f0c7d80f9c860a7c9b900
account :101

sign : 0x7a9a61970653d45313476352ca55ac24ae772d7582f87ff8e1afa8422c982fbd56d4d8e84dbafa2535cea16a44da382319a40ae63103157e6f6a2311a03dbb5100
account :100

sign : 0xbe2ae071937f6c69af65546d48504cfbb0bcc2868acd9cf540e4e609588efcc97ce0aa561f22705bb7761806671de3ae3d66a210f0cbd1c427803e780212000d01
account :100
Thread started: <Thread Pool> #11

sign : 0x283024a0abf1522a474f02394222a4a8831e9fa4ecb1567ad0d9f7ff0abdd10f4e1910df31cd9cdf645ef23f7d3d4576d3bd63e6ddd37326b8b05a09ba846f5d00
account :100

sign : 0xc64da10930f514642a40841320efd0cd2089bd44fe13f8f0de5bde3d78ca8d1c3a63daf9b181687d60fa276a75a7d63e678bf3148b5442b2a601989526b5619100
account :100

sign : 0xfff9ff820dac1f09d2a2e212296458a5e5b01062fdd61c6b40479228beb2303f6c6720cde696e19af035b4734c619be52692ac411480c32a509429bcca2a405e00
account :100

sign : 0xb26f509a86bc722e261b0d514da9c92e3d5a958a611437ff02a04b6ef928a3e968d5b43f731125fcfd78811bc2d1ca51df0a218087c0c3bf5c91561fea16716001
account :100

sign : 0xfeafb647d57e7880acba71d2300192a1abe65ab8773ea8969716e3c7b645104240b4fe5760977f21300b13f014a72bd10ef6c2de592e922286e8453457193f5901
account :100

sign : 0x42ab7021eb66a03076608d417df332b3239b34b646ed4bde368e3524c8adaf7162eaa2b38a2177a657372902f19869726503277743533034eb2e824e3583516f00
account :100
sign : 0xe7f89fad73e077576427548093d7368b742341bfa6f6241604d6e8f96b69df153c0ab6fb6c1c9212bc8ff6fe7bad26f73209f8cf4fc0edd90d740c47d8aa29b401
`

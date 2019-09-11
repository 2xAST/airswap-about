A library contract of protocol structs. [View the code on GitHub](https://github.com/airswap/airswap-protocols/tree/master/protocols/swap).

# `Order`

| Param     | Type      | Description                                     |
| :-------- | :-------- | :---------------------------------------------- |
| nonce     | `uint256` | Unique per maker and should be sequential       |
| expiry    | `uint256` | Expiry in seconds since 1 January 1970          |
| maker     | `Party`   | Party to the trade that sets terms              |
| taker     | `Party`   | Party to the trade that accepts terms           |
| affiliate | `Party`   | Party compensated for facilitating \(optional\) |

# `Party`

| Param  | Type      | Description                        |
| :----- | :-------- | :--------------------------------- |
| wallet | `address` | Wallet address of the party        |
| token  | `address` | Contract address of the token      |
| param  | `uint256` | Value \(ERC-20\) or ID \(ERC-721\) |
| kind   | `bytes4`  | Interface ID of the token          |

# `Signature`

| Param   | Type      | Description                                                                               |
| :------ | :-------- | :---------------------------------------------------------------------------------------- |
| signer  | `address` | Address of the wallet used to sign                                                        |
| v       | `uint8`   | `v` value of an ECDSA signature                                                           |
| r       | `bytes32` | `r` value of an ECDSA signature                                                           |
| s       | `bytes32` | `s` value of an ECDSA signature                                                           |
| version | `bytes1`  | [EIP-191](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-191.md) signature version |

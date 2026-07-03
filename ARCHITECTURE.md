The smart contract architectural guide:

The smart contract will be built in such a way that the default balance state is stored as a nested mapping of the token being held to user address to balances.

Then you have:
1. A stake field for users that stake a particular token in the contract.
2. Another field for storing admin addresses, both as a list and as a mapping.
3. A field for mapping of token addres to total stake balance.

The contract will be able to transfer tokens across different addresses. The smart contract will be able to transfer a token and deduct the balances from the addresses.

The contract will store users' addresses as sub-addresses that will be created on account creation. It uses CREATE2 for creating sub-addresses under the contract address.

The idea of the contract is a CEX wallet.

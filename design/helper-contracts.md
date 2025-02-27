# Helper Contracts

With the [universal-token-router.md](universal-token-router.md "mention") taking care of token approval, the entire Derion's peripheral contracts system can be freely updated to continuously improve the user experience with the protocol.

**Helper** calculates the target state from transaction input to accommodate market state slippage.

**TokenDescriptor** defines the metadata for each [EIP-6120](https://eips.ethereum.org/EIPS/eip-6120) ID.

**FeeReceiver** takes and manages the protocol fee (in [funding-rate.md](../protocol/funding-rate.md "mention")).

Those helper contracts are not part of the Derivable protocol, and Derivable core contracts are designed to work properly with any malfunctioned or malicious helper contracts specified by the application front-end and its users.

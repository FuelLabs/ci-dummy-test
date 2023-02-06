# MessageOut

```rust,ignore
use fuel_types::{MessageId, Bytes32, Address};
pub struct MessageOut {
    pub message_id: MessageId,
    pub sender: Address,
    pub recipient: Address,
    pub amount: u64,
    pub nonce: Bytes32,
    pub len: u64,
    pub digest: Bytes32,
    pub data: Vec<u8>,
}
```

- A `MessageOut` receipt is generated as a result of the `send_message()` Sway method in which a message is sent to a recipient address along with a certain amount of coins.
- The `data` field currently supports only a vector of non-reference types rather than something like a struct.
- [Read more about `MessageOut` in the Fuel protocol ABI spec](https://github.com/FuelLabs/fuel-specs/blob/master/src/protocol/abi/receipts.md#messageout-receipt)
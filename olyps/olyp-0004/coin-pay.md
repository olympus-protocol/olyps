Coins (Pay) Verification Flow
--------------

### Payload elements definitions

 Name | Type 
---|---
[Type](#type) | PaymentType
[TxIn](#txin) | []Intputs
[TxOut](#txout) | []Outputs  
 
#### Type

The Type element defines the verifications this specific payment type needs to check. It can be `pay-to-network`, `pay-to-proposals` or `pay-profits`.

#### TxIn

The TxIn element is an array of Inputs.

Each input is a reference to a utxo that is being spent on the transaction, the inputs information variates depending on the `Type`.

* `pay-to-network`: The user pays a specific amount to the network for a service. User requires to sign the input to prove ownership.
* `pay-to-proposals`: The network uses the budget utxos to pay the proposals, it needs a reference to the input but no signature is required.
* `pay-profits`: The network consumes all the `pay-to-network` utxos and pays to the entire worker list. Signatures are not required.

#### TxOut
 
The TxOut element is an array of Outputs.
 
Each output is a reference to the new coin owner. It consists of a value and a Public Key Hash for new coin ownership.
 
### Verification


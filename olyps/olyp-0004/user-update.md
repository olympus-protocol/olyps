User (Update) Verification Flow
--------------

### Payload elements definitions

Name | Type 
--- | --- 
[PubKey](#pubkey) | [48]byte 
[NewPubKey](#newpubkey) | [48]byte
[Sig](#sig) | [96]byte 
[Name](#name) | string 

#### PubKey

The PubKey is the BLS12-381 serialized public key that is related to the current user name.

#### NewPubKey

The NewPubKey is the BLS12-381 serialized public key that replaces the old public key.

#### Sig

The Sig is the BLS12-381 serialized signature is the aggregated signature of the two signatures of both public keys using the Name as the message.

#### Name

The Name is the user identifier.

### Verification

[![alt](./img/user-update.svg)](./img/user-update.svg?raw=true&sanitize=true)

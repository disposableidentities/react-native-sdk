# A React Native SDK for Disposable ID

## Abstract Method Specification

### Identity

#### initializeDisposableIdentityAccount

This creates a Hierarchical Deterministic Wallet account - depth=1 - from a master node - depth=0 - from a master seed (cfr. https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki) for a **Disposable Identity Wallet**.
This is a one-time operation (should be invoked only once).

#### createMainDID

This creates a wallet chain - depth=2 - from the Disposable Identity Wallet account and uses the public key as "method-specific-id" (as defined in https://www.w3.org/TR/did-core/#did-syntax) and uses the "method-name" *"disposable:D2"*.

Example (input):
(todo)

Example (output):
```
"did:disposable:D2:1BvBMSEYstWetqTFn5Au4m4GFg7xJaNVN2"
```

The same method also creates a DID Document, formatted according to https://www.w3.org/TR/did-core/).
Direct link to an example from that W3C spec: https://www.w3.org/TR/did-core/#real-world-example

(TODO later to define exactly how a Disposable DID Document will be formatted)

#### createDisposableDID

This creates a address - depth=3 - from a Main DID where this address is used as "method-specific-id" for the Disposable DID and the "method-name" is *"disposable:D3"*.

The "input" for this method is a Main DID (see previous).

Example (output):
```
"did:disposable:D3:12eMAv9Di2H9VaNjZX2sNwPFbe7TT4KX1a"
```

#### getDIDDocument
(TODO)
#### deleteDisposableDID
(TODO)
#### generateDataVerifiableCredential
(TODO)
#### generateConsentVerifiableCredential
(TODO)
#### createVerifiableCredentialsPackage
(TODO)

### Barcode/markers
(TODO Jari)

### AI
(TODO ?)

## React Native Method Specification

### Identity
(TODO ?)

### Barcode/markers
(TODO ?)

### AI
(TODO ?)

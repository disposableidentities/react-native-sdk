# A Mobile SDK for Disposable ID

## Abstract Method Specification

### Identity

#### initializeDisposableIdentityAccount

This creates a key account for a **Disposable Identity Wallet**.
This is a one-time operation (should be invoked only once).

Next to account creation, this method also:
* creates a an in-app key store
* creates x amount remote private key stores (for backup)
* saves the keys in the in-app key store
* saves the keys in the remote private key stores
* creates an in-app document store
* creates a chain for this account
* creates x amount remote document stores linked to the account chain

#### createMainDID

This creates a public key from an Identity Wallet account and uses the public key as "method-specific-id" (as defined in https://www.w3.org/TR/did-core/#did-syntax) and uses the "method-name" *"disposable:mainDID"*.

Example (input):
```
"1BvBMSEYstWetqTFn5Au4m4GFg7xJaNVN2"
```
Example (output):
```
"did:disposable:mainDID:1BvBMSEYstWetqTFn5Au4m4GFg7xJaNVN2"
```
Next to creation of a Main DID, this method also:
* creates a DID Document, formatted according to https://www.w3.org/TR/did-core/). Direct link to an example from that W3C spec: https://www.w3.org/TR/did-core/#real-world-example. (TODO later to define exactly how a Disposable DID Document will be formatted)
* saves the DID Document in the account in-app key store
* saves the DID Document in the account remote document stores
* add the DID Document hash to the account chain
* saves the hash in the account in-app key store
* saves the hash in the account remote document stores

#### createDisposableID

This creates a coconut credential from a main DID to be used as Disposable ID with  "method-name" *"disposable:ID"*.

Example (input):
```
"did:disposable:mainDID:1BvBMSEYstWetqTFn5Au4m4GFg7xJaNVN2"
```
Example (output):
```
"did:disposable:ID:12eMAv9Di2H9VaNjZX2sNwPFbe7TT4KX1a"
```
Next to creation of the Disposable ID, this method also:
* creates the coconut credential proof JSON document
* stores this coconut credential proof JSON document in the account in-app document store
* stores this coconut credential proof JSON document the account remote document stores

Important note: A Disposable ID and coconut credential proof JSON document are not added to a chain.

#### createDisposableDataExchangeChannel
(TODO)
#### closeDisposableDataExchangeChannel
(TODO)
#### reopenDisposableDataExchangeChannel
(TODO)

#### verifyDisposableIDViaDataExchangeChannel
(TODO)

#### getDIDDocumentbyDID
(TODO)
#### verifyDID
(TODO)
#### getHashByDID
(TODO)
#### getDIDDocumentByHash
(TODO)



#### generateDataVerifiableCredential
(TODO)
#### generateConsentVerifiableCredential
(TODO)
#### createVerifiableCredentialsPackage
(TODO)
#### shareVerifiableCredentialsPackageViaDataExchangeChannel
(TODO)
#### deleteDataVerifiableCredentialViaDataExchangeChannel
(TODO)
#### updateDataVerifiableCredentialStatus
(TODO)

#### sendVerifiableCredentialRequestToExternalIssuerViaDataExchangeChannel
(TODO)
#### receiveVerifiableCredentialFromExternalIssuerViaDataExchangeChannel
(TODO)
#### showVeriableCredentialViaDataExchangeChannel
(TODO)

#### provideKeysToCustodians
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

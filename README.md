# FreeID

[freeid.me](https://www.freeid.me/)

Open and free specification of FreeID.

## Verifiable Credential example

The FreeID VC should hold the following information:

- Unique VC ID
- Issuer DID and Name
- Issuance date
- Subject DID
- Subject Name
- Subject Date of Birth
- Subject Gender

```
{
  "@context": [
    "https://www.w3.org/2018/credentials/v1"
  ],
  "type": ["VerifiableCredential", "IdentityCredential"],
  "id": "urn:credential:240720-0-0001",
  "issuer": {
    "id": "did:example:76e12ec712ebc6f1c221ebfeb1f",
    "name": "Liberstad FreeID Verification Service"
  },
  "issuanceDate": "2024-07-20T13:58:53Z",
  "credentialSubject": {
    "id": "did:example:88e12ec712ebc6f1c221ebfeb1f",
    "name": "Jane Doe",
    "dateOfBirth": "1984-01-20",
    "gender": "Female"
  },
  "proof": {}
}
```

## Open Questions

Should the type be `IdentityCredential` or `IDCard`? The latter is used for examples by Auth0.

## Resources

[VC Data Model](https://www.w3.org/TR/vc-data-model/)
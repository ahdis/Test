# Create Medication Card document

In a primary system, different medications are documented in a treatment context. Primary systems can use this transaction to generate a Medication Card document with the help of the Content Creator.

```
1 Test
2 Test2
```
#### Request Message

The following snippet is taken from a sample request recorded during the EPR projectathon in September 2020. Some elements
were ommitted to increase readability. The raw request file may be found
**[here](../Auth_samples/04_AuthnRequest_raw.xml)**.

The *AuthnRequest* conveys the following information to be set by the primary system:
- *ID*: A unique ID of the request message (line 7 in the example below).
- *Issuer*: A ID of the primary system as URL (line 9 in the example below).
- *SignedInfo*: Signature metadata and the digest value used for the signature.
- *SignatureValue*: The signature of the request (line 23 in the example below).
- *X509Certificate*: The X509 certificate used to sign the request (line 26 in the example below).

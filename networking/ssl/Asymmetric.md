### Asymmetric Keys

- Private Key : Is always kept secret; only owners knows about it.
- Public Key  : 

#### Purpose
- Used for Encryption: Data is encrypted using public key and decrypted using private key.
 
 - Signing Data using Private Key: Data is signed(Hashed) using Private key and this signature can be verified using public key.


 #### Asymmetric Encryption 
  ![Asymmetric!](\networking\ssl\images\asymmetric.PNG)

#### Asymmetric Data Signing
We want reciver of the data to be 100% sure that the data is receieved from intented sender.
![AsymmetricSign!](\networking\ssl\images\asymmetricSigning.PNG)


#### RSA Algorithm
- Uses Private/Public (Asymmetric) Keys
- Used for encryption, signature

#### PKI - Public Key Infrastructure
- Set of different algorithms, certifcates, entities  that allows communication based on certificates(trust) relation.
- Every entity in PKI has its own public key.
- This public key is trusted by every other entity

#### Elements of PKI
- CA : Assign certifcates or delegate trust to intermediate CAs 
- Intermediate CAs : Assgins certificate
- Certifcate : Used to secure site, vpn
- Every entity in PKI has its own public key.
- This public key is trusted by every other entity



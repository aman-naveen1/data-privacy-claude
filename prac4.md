PRACTICAL – 4

IMPLEMENTATION AND STUDY OF CRYPTOGRAPHIC TECHNIQUES
AIM

To study and implement basic cryptographic techniques such as encryption, hashing, and digital signatures, and to understand their importance in protecting data privacy, confidentiality, integrity, and authenticity.

OBJECTIVES

To understand the basic concept of cryptography.

To understand encryption and decryption.

To study symmetric and asymmetric cryptography.

To understand hashing and its applications.

To understand digital signatures.

To implement basic cryptographic operations using Python.

To understand the role of cryptography in data privacy.

INTRODUCTION

Cryptography is the science of protecting information by transforming it into a form that unauthorized people cannot easily understand.

Cryptography is widely used to protect information transmitted over the internet, stored on computers, and exchanged between users and applications.

The major cryptographic techniques studied in this practical are:

Encryption

Decryption

Hashing

Digital signatures

Encryption provides confidentiality by converting readable data, called plaintext, into an unreadable form called ciphertext.

Decryption converts ciphertext back into plaintext.

Hashing converts data into a fixed-length value called a hash or digest. Hash functions are designed so that small changes in the input produce a different output.

Digital signatures can be used to verify the authenticity and integrity of digitally signed information.

REQUIREMENTS

Hardware:

Computer/Laptop

Minimum 4 GB RAM

Keyboard and mouse

Software:

Python 3.x

Python IDE or Visual Studio Code

Command Prompt/Terminal

Python libraries:

hashlib

cryptography

THEORY

5.1 SYMMETRIC ENCRYPTION

Symmetric encryption uses the same secret key for encryption and decryption.

Example:

Plaintext + Secret Key
|
v
Encryption
|
v
Ciphertext
|
v
Decryption
|
v
Plaintext

Advantages:

Fast

Suitable for large amounts of data

Relatively efficient

Disadvantage:

The secret key must be securely shared between the parties.

5.2 ASYMMETRIC ENCRYPTION

Asymmetric cryptography uses a pair of keys:

Public key

Private key

The public key can be shared, while the private key must be protected.

Asymmetric cryptography is commonly used for secure communication, authentication, and digital signatures.

5.3 HASHING

A hash function converts input data into a fixed-length output.

Example:

Input:
Hello World

SHA-256 Hash:
A cryptographic hash value is generated from the input.

A hash is generally not intended to be decrypted back into the original message.

Hashing can be used for:

Integrity verification

Password storage systems

File verification

Digital signatures

5.4 DIGITAL SIGNATURE

A digital signature is a cryptographic mechanism used to verify the authenticity and integrity of digital information.

A simplified process is:

Message
|
v
Hash Function
|
v
Message Digest
|
v
Sign with Private Key
|
v
Digital Signature

The receiver can use the corresponding public key to verify the signature.

EXPERIMENT 1 – SHA-256 HASHING

AIM:

To generate a SHA-256 hash of a given message using Python.

PROGRAM:

import hashlib

message = "Hello World"

hash_value = hashlib.sha256(message.encode()).hexdigest()

print("Original Message:", message)
print("SHA-256 Hash:", hash_value)

PROCEDURE:

Open Python IDE.

Import the hashlib library.

Store the message in a variable.

Convert the message into bytes using encode().

Apply the SHA-256 hashing algorithm.

Convert the resulting hash into hexadecimal form.

Display the original message and hash value.

Change one character in the message and run the program again.

Compare the two hash values.

EXPECTED OBSERVATION:

The original message produces a fixed-length SHA-256 hash.

If even one character of the message is changed, the resulting hash will be substantially different.

RESULT:

The SHA-256 hashing algorithm was successfully implemented and the effect of changing the input message was observed.

EXPERIMENT 2 – FERNET ENCRYPTION AND DECRYPTION

AIM:

To implement symmetric encryption and decryption using Python's cryptography library.

PROGRAM:

from cryptography.fernet import Fernet

key = Fernet.generate_key()

cipher = Fernet(key)

message = b"Data Privacy Practical"

encrypted_message = cipher.encrypt(message)

decrypted_message = cipher.decrypt(encrypted_message)

print("Original Message:", message.decode())
print("Encrypted Message:", encrypted_message.decode())
print("Decrypted Message:", decrypted_message.decode())

PROCEDURE:

Install the cryptography library if it is not already installed.

Import Fernet from the cryptography library.

Generate a secret key.

Create a Fernet cipher using the key.

Define the original message.

Encrypt the message using the cipher.

Display the encrypted message.

Decrypt the encrypted message using the same key.

Display the decrypted message.

Compare the original and decrypted messages.

EXPECTED OUTPUT:

Original Message: Data Privacy Practical

Encrypted Message: [Encrypted ciphertext]

Decrypted Message: Data Privacy Practical

OBSERVATION:

The encrypted message is not readable as ordinary text. When the correct key is used, the ciphertext can be decrypted back into the original message.

RESULT:

Symmetric encryption and decryption were successfully implemented using the Fernet encryption mechanism.

EXPERIMENT 3 – DIGITAL SIGNATURE

AIM:

To generate and verify a digital signature using a private/public key pair.

PROGRAM:

from cryptography.hazmat.primitives.asymmetric import rsa, padding
from cryptography.hazmat.primitives import hashes

private_key = rsa.generate_private_key(
public_exponent=65537,
key_size=2048
)

public_key = private_key.public_key()

message = b"Data Privacy Practical"

signature = private_key.sign(
message,
padding.PSS(
mgf=padding.MGF1(hashes.SHA256()),
salt_length=padding.PSS.MAX_LENGTH
),
hashes.SHA256()
)

print("Digital Signature Generated Successfully.")

public_key.verify(
signature,
message,
padding.PSS(
mgf=padding.MGF1(hashes.SHA256()),
salt_length=padding.PSS.MAX_LENGTH
),
hashes.SHA256()
)

print("Signature Verification Successful.")

PROCEDURE:

Generate an RSA private key.

Generate the corresponding public key.

Create the message.

Generate a digital signature using the private key.

Use the public key to verify the signature.

Observe the verification result.

Modify the message and repeat the verification.

Observe that verification fails when the message is changed.

EXPECTED OUTPUT:

Digital Signature Generated Successfully.

Signature Verification Successful.

OBSERVATION:

The signature verifies successfully when the original message is used.

If the message is modified after signing, the signature verification

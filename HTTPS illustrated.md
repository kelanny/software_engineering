# HTTPS Illustrated

HTTPS is  an extension of the the [[HTTP Protocol]].
It is a part of the protocol that helps to encrypt and secure a connection between a [[client]] and a [[server]].
Without HTTPS, the connection between [[server]] and [[browser]] is in plain text and anyone with access to the connection can read the data sent.
[[HTTPS]] was designed to encrypt the data sent between a sender and a receiver to make it unreadable.
[[HTTPS]] encrypts the connection using [[TLS]].


### How TLS handshake works
##### Step 1: TCP Connection 
In this step, the [[Browser]] establishes a [[TCP Connection]] with the [[server]]

##### Step 2: TLS handshake - Certificate check
- In this step,  the [[client]] and the [[server]] exchanges the Hello Messages

##### Step 3: Key Exchange

- The [[client]] generates a session key 
-  Using the [[Asymmetric Encryption]] the [[client]] encrypt the session key with the  [[Public Key]] included in the certificate and send it to the [[server]]
- The server decrypts the session key data using its [[Private Key]]

##### Step 4: Data Transmission
In this step,  both having the session key, they agree on the Cipher Spec and they start to transmit data back and forth encrypted using [[Symmetric Encryption]]

##### Why use both [[Asymmetric Encryption]] and [[Symmetric Encryption]]  to transmit data ?
The reason for this is, [[Asymmetric Encryption]] is computationally expensive and therefore not suitable for bulk data transmission


- The Hashing used in this example is [[TLS 1.2]]
	-  [[TLS 1.2]] Takes 2 network route trips 
- The latest version is [[TLS 1.3]]
	- Supported on all major browsers
	-  Optimizes the handshake to reduce the number of network round trips to 1
	-  RSA not supported for encryption
	



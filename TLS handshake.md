### Step 1:  [[TCP Connection]] - [[TCP Handshake]]


### Step 2: Client-Server Hello Messages

##### Client Hello Message
 - In the Hello message, the client tell the server the following information
	1.The [[TLS Version]] it can support
	2.Cypher suite it support
##### Server Hello Message
	- The [[server]]  chooses the [[TLS Version]] to use based on the ones the browser can support.
	- It sends this information back to the client as a Server Hello message

	- The [[server]] sends the [[certificate]] to the [[client]]
		This certificate includes alot of information relating to the server but amongst those, it send its [[Public Key]]
		 The client uses the received [[Public Key]] in [[Asymmetric Encryption]]
	- This step concludes the Server hello message
	 
	 
	

	
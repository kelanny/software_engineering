1. [[DNS Server ]] Request and [[IP Addresses]] resolution
	- The browser sends a DNS request to the DNS server to resolve www.google.com with an [[IP Addresses]]
1. [[browser]] sends the http request to the server
	- 
	- It converts the [[URL]] to a [[HTTP]] request message and sends it the data to the [[server]] 
3. [[server]] receives the request and sends back a http response with the data requested


Have you ever paused to ponder what unfolds behind the scenes when you enter a URL into your browser and hit enter?
Its a fascinating journey that involves a symphony of technology seamlessly orchestrating the retrieval of the web content. Let's embark on a journey together and zoom on the intricate process that occurs when you type  **https://www.google.com** in your browser.

### DNS Request
The journey begins with the [[Domain Name System]]. The browser seeks to translate the human-readable domain name "www.google.com" into a corresponding [[IP Addresses]] associated with Google's [[server]].

### TCP/IP
Browser establishes a [[Transmission Control Protocol (TCP)]] connection with google [[server]] 
 using [[Internet Protocol (IP)]]. The [[TCP-IP]] governs the rules of transmitting data packets accross the internet, ensuring reliable communication between your browser and the [[server]]

### Firewall
Before the request get's to the google server,  it traverse through a  [[firewall]]. 
The firewall scrutinizes the request to verify compliance with the security criteria before granting passage

HTTPS/SSL

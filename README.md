
## Why Web Security is important :

When data transfer happens through http over the internet, some one can easily decode the data and get all the content.
So to build a secure transaction medium web security is essential. We can achieve web security by adding an SSL certificate which is provided by a Certificate Authority(CA)/
They look into the company details , verify and provide a certificate. The certificate has to be installed on the web server.

When a client interacts with the web server, during the handshake process the server sends one of the key(public key) back to the client.
Client uses that key to encrypt the data and sends the data back to the server. The server holds another(private key) which is used to decode the data.

When the data trasfer happens via https the data is normally encrypted and can't be decrypted by anyone except the server.

The point which is very important to remember is that only private key can decrypt the data encrypted by the public key.

When a website shows a pad lock or a green color symbol with https tells us that the web site is secured.

## TrustStore and KeyStore
- KeyStore is used by the server to store the private keys where as TrustStore is used to store the certificate 
  from Certificate Authorities(CA).  
  
They KeyStore can be generated by a commandline tool in our own machine like keytool.

For example : Generating a certificate for 365 days.

keytool -genkey -alias spring-https-example -storetype JKS -keystore spring-https-example.jks -keyalg RSA -keysize 2048 -validity 365 

  


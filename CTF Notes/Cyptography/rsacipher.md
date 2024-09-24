# RSA cipher

- RSA algorithm is an asymmetric cryptography algorithm. Asymmetric means that it works on two different keys i.e. Public Key and Private Key. As the name describes the Public Key is given to everyone and the Private key is kept private.

## An example of asymmetric cryptography: 

1. A client (for example browser) sends its public key to the server and requests some data.
2. The server encrypts the data using the client’s public key and sends the encrypted data.
3. The client receives this data and decrypts it.

> Since this is asymmetric, nobody else except the browser can decrypt the data even if a third party has the public key of the browser.

* The idea of RSA is based on the fact that it is difficult to factorize a large integer.
* The public key consists of two numbers where one number is a multiplication of two large prime numbers.
* The private key is also derived from the same two prime numbers.

So if somebody can factorize the large number, the private key is compromised. Therefore encryption strength lies in the key size and if we double or triple the key size, the strength of encryption increases exponentially. RSA keys can be typically 1024 or 2048 bits long, but experts believe that 1024-bit keys could be broken shortly. But till now it seems to be an infeasible task.

### Tools to use for RSA encryption / decryption

- [DecodeFr](https://www.dcode.fr/rsa-cipher)


#### Sources

- https://www.geeksforgeeks.org/rsa-algorithm-cryptography/
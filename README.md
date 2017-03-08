# RSA-encryption

Because we are studying number theory in mathematics, I aimed to create a program to encrypt and decrypt messages using the RSA algorithm. For most of history, encryption methods have placed their security on a hidden key. If this key were known, it would be easy to decrypt any message. With this encryption method, we have a public key that anyone can see. The security relies on that fact that factoring sufficiently large numbers is extremely hard. This code was used for encrypting data in my internship.

To learn more:
https://wikipedia.org/wiki/RSA_(cryptosystem)

	
How to Use
---------- 
1. Create an instance of `RSAKeyGenerator`.
2. Call the `makeKey()` method, passing in a constant to specify which kind of key should be returned.
   * `RSAKey.PUBLIC_KEY` for encrypting
   * `RSAKey.PRIVATE_KEY` for decrypting
   * `RSAKey.COMPLETE_KEY` for efficient decryption using the Chinese Remainder Theorem
3. Cast the `RSAKey` returned to the appropriate type of `RSAKey`.
   * `RSAPublicKey`
   * `RSAPrivateKey`
   * `RSACompleteKey`
4. Call the key's `use()` method, passing in the source and destination file paths.
   * the key will perform it's operation on the file specified by `source`
   * the key will write the result of it's operation to the file specified by `destination`
  
Author
------
  * Andrew Martin

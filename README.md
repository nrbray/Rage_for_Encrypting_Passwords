# Rage (age) encryption basic example for password protected encrypted file  

- gen-local-key creates age keypair with private identity key encrypted by user entered password to local-key file and adds the public recipient key to the recipients-file
  - <stdin, >>recipients-file, >local-key
- encrypt takes a single line of user entered 'secret' text input and encrypts it to the encrypted file with the age public recipients from the recipients file
  - <stdin, <local-key, >encrypted
- decrypt places the decrypted text in the Xclipboard from the encrypted file and user entered password to unlock the private identity using local-key
  - <encrypted, <stdin, <local-key, >(pastebuffer)

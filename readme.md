[ChatGPT]()

## Encrypte/Cipher the `.env` into `.env.gpg`
```bash
gpg --symmetric --cipher-algo AES256 .env
```
###### Give the secret password(passphrase) to complete the encryption
### push `.env.gpg` to GitHub. Not `.env`

## Decrypt/Decipher the `.env.gpg` into `.env`
```bash
gpg --decrypt .env.gpg > .env
```
###### Give the secret password(passphrase) to complete the Decryption

## You can clear the cache to force GPG to ask for the passphrase:
```bash
gpgconf --reload gpg-agent
```

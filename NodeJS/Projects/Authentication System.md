## Building a authentication system with different categories.
1. A way for users to signup and signin into the application. They cannot signup or signin using public mails. Only Private mails are allowed.
2. They are allowed to choose the categories, and based on that categories user will be allocated with the roles.

### JWT (Json Web Token)
1. Public Key & Private Key cryptography: Whatever things we encrypt using public key can only be decrypted by our private key. Private key is not meant to be shared.
2. Stateless and State-full mechanism: Stateless means any particular data is not stored somewhere in the database, that data is only with user. Whereas State-Full means the data is stored somewhere in the database.
3. JWT tokens are comprised of three parts, One is Header(Algorithm Section) i.e. Our data is going to be encrypted using some algorithm.
## Passport library
1. Passport library is used for session management. 
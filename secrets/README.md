# Secrets
Temporary local storage for exporting symmetric secret keys.

For my tests I'm using `git-crpyt export-key shared.key` to generate a secret key.
This key would need to be securely shared with contributors.

## Limitations
- If the key were ever compromised, then all the secret keys in the repository would become vulnerable.
- If the key were ever lost, a new key can only be generated from a user who has unlocked the repository.
Attempting to create a new key when git-crypt has locked the repository results in the following error:
```
Error: Unable to open key file - have you unlocked/initialized this repository yet?
```

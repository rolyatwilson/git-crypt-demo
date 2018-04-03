# git-crypt-demo
[git-crypt](https://github.com/AGWA/git-crypt) is incredibly easy to use.
I wanted to see specifically how easy it is to encrypt all files within a directory.
[private-data](private-data) contains a single `.gitattributes` file that tells git-crypt to encrypt all files in that directory except the `.gitattributes` file.
This successfully encrypts the [secret.key](https://github.com/rolyatwilson/git-crypt-demo/blob/master/private-data/secret.key) file.

## Limitations
Unintended commits to `.gitattributes` can break all the things.
[https://github.com/rolyatwilson/git-crypt-demo/pull/1] illustrates how a single 1 character change to `.gitattributes` prevents any new secret files from being encrypted.

[https://github.com/rolyatwilson/git-crypt-demo/pull/2] illustrates how that same 1 character change will unencrypt the existing secrets file when an update is pushed up.

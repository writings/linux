Basics on SSH
=============
Generate our key on the local machine:

`ssh-keygen [params for algo] ~/.ssh/name-of-key`

Use the key:

* ssh-agent $SHELL
* ssh-add
* ssh-add -L (to list used keys)

Add our pubkey to the remote machine:

* `ssh-copy-id -i USERNAME@HOSTNAME` (if using key)
* `ssh-copy-id -i ~/.ssh/name-of-key USERNAME@HOSTNAME` (if not)
* ssh USERNAME@HOSTNAME (to test that password isn't asked)

*If it fails, make sure to chmod +755 ~/.ssh and authorized\_keys on the remote machine.*


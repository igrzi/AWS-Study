# Key Pairs

## What are key pairs?

Key pairs, as the name suggests, it's a form to associate a ***key to a value***, this key pair is used to Encrypt and Decrypt EC2 Instance login informations.

* In MS Windows instances, in creating it will require a key to configure login and/or decrypt a password.

* In Unix like systems, login information by SSH keys are stored inside of an archive ```~/.ssh/authorized_keys```.

All Amazon EC2 keys are of the SSH-2 RSA type, with 2048 bits of size. You can also have at maximum of 5000 key pairs per region. 

***AWS only stores the public key.***
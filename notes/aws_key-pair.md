# Key Pairs

## What are key pairs?

Key pairs, as the name suggests, it's a form to associate a ***key to a value***, this key pair is used to Encrypt and Decrypt EC2 Instance login informations.

- In MS Windows instances, in creating it will require a key to configure login and/or decrypt a password.

- In Unix like systems, login information by SSH keys are stored inside of an archive ```~/.ssh/authorized_keys```.

All Amazon EC2 keys are of the SSH-2 RSA type, with 2048 bits of size. You can also have at maximum of 5000 key pairs per region. 

***AWS only stores the public key.***

## SSH Key Generation

```ssh-keygen -t rsa -b 2048```

- ```ssh-keygen```: This is the basic command to start the SSH Key creation.

- ```-t rsa```: This specifies the type of key to be generated.

- ```-b 2048```: This sets the number of bits in the key, the size of ***2048*** is common for RSA keys.

**You only show to others your public SSH key**. ***NEVER SHOW OR SHARE YOUR PRIVATE SSH KEY***.
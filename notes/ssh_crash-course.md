# SSH | Secure SHell 

## What is SSH?
- Secure Shell.

- Communication Protocol (Like http, https, ftp, etc).

- Encrypted shell communication with a linux server.

## Client/Server Communication
- SSH is the client

- SSHD is the server (Open SSH Daemon).

- The server must have SSHD installed and running.

## Authentication Methods

- Password.

- SSH Public / Private Key Pair, this is the recommended method.

- Host Based.

## Generating Keys

```bash
ssh-keygen -t rsa
```

This will create a *SSH public key* and a *SSH private key* of RSA type. You key will be located in your home directory inside the .ssh folder.

- ~/.ssh/id_rsa | This is your ***PRIVATE KEY***.
- ~/.ssh/id_rsa.pub | This is your ***PUBLIC KEY***.

- The public key goes into a file in .ssh/authorized_keys inside your instance.

If the private key is in my computer, I can ssh directly into my instance without specifying a path for the private key.
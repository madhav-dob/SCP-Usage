
# SCP (Secure Copy) Command Usage

## Overview

This readme provides a guide on using the SCP (Secure Copy) command to copy files between a local machine and a remote server securely. SCP is a protocol built on top of SSH (Secure Shell) and allows for secure file transfers.

## Prerequisites

Before using SCP, ensure that:

1. **SSH is Installed:** Both the local machine and the remote server should have SSH installed.

2. **Access Credentials:** You should have the necessary access credentials (username and password or private key) for the remote server.

## Usage

### Copying from Local to Remote

To copy a file from the local machine to a remote server, use the following command:

```bash
scp /path/to/local/file username@remote_server:/path/to/destination/
```


### Copying from Remote to Local

To copy a file from a remote server to the local machine, use the following command:

```bash
scp username@remote_server:/path/to/remote/file /path/to/destination/
```

- Replace `username` with your username on the remote server.
- Replace `remote_server` with the IP address or domain of the remote server.
- Replace `/path/to/remote/file` with the path to the file on the remote server you want to copy.
- Replace `/path/to/destination/` with the local path where you want to copy the file.

### Copying with a Specific Port

If your SSH server uses a non-default port (not 22), specify the port with the `-p` option:

```bash
scp -P port_number /path/to/local/file username@remote_server:/path/to/destination/
```

or

```bash
scp -P port_number username@remote_server:/path/to/remote/file /path/to/destination/
```

- Replace `port_number` with the actual port number.

## Examples

### Copying from Local to Remote

```bash
scp ~/Documents/example.txt user@192.168.1.100:/home/user/documents/
```

This command copies the local file `example.txt` to the remote server at the specified destination.

### Copying from Remote to Local

```bash
scp user@192.168.1.100:/home/user/documents/example.txt ~/Downloads/
```

This command copies the remote file `example.txt` to the local machine's Downloads folder.

## Conclusion

Using SCP provides a secure and efficient way to transfer files between your local machine and a remote server. Incorporate these commands into your workflow to streamline file management across different environments.
```

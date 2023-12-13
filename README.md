## What is Ansible Vault?

Ansible Vault is a feature that enables users to encrypt values and data structures within Ansible projects. This ensures the security of sensitive data when running Ansible playbooks.

This feature provides the ability to secure sensitive data and keep it safe.

The Ansible Vault feature offers several options for working with encrypted data:

- Create
- Decrypt
- Edit
- View
- Encrypt
- Encrypt_string
- Rekey

### Create New Encrypted Files
To create an encrypted file with Ansible Vault, use the 'create' option. For example:

```bash
ansible-vault create vault.yml
```

You will be prompted to enter a password for the vault and confirm it. A code editor will then open, allowing you to write content to be encrypted. Save the file and exit to create a new file with encrypted data (`vault.yml`).

### Decrypt Files
If you have an encrypted file and need to decrypt it, use the 'decrypt' option. For example:

```bash
ansible-vault decrypt vault.yml
```

You will be prompted to enter the vault password to decrypt the file.

### View Encrypted Files
To view decrypted data without changing the file, use the 'view' option. For example:

```bash
ansible-vault view vault.yml
```

You will be prompted to enter the vault password to decrypt and view the file. The original encrypted file remains unchanged.

### Encrypt Files
To encrypt a file and its data, use the 'encrypt' option. For example:

```bash
echo "hello my name is Moein" >> greeting.txt
ansible-vault encrypt greeting.txt
```

You will be prompted to enter and confirm a password for the encryption. Upon successful encryption, the file will contain encrypted data.

### Change the Password of Encrypted File
To change the password of an encrypted file, use the 'rekey' option. For example:

```bash
ansible-vault rekey greeting.txt
```

You will be prompted to enter the previous password and the new password. Upon successful entry, a message "Rekey successful" will be displayed.

----

[reference](https://www.digitalocean.com/community/tutorials/how-to-use-vault-to-protect-sensitive-ansible-data)
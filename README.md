### what's ansible-vault ? 

Ansible Vault is a feature that allows users to encrypt values and data structures within Ansible projects. 

This feature provides the ability to secure sensitive data and keep it safe.

We can use this feature when we want to run an ansible playbook .

This ability is called `ansible-vault` and has several options to use it 

<ol>
  <li>create</li>
  <li>decrypt</li>
  <li>edit</li>
  <li>view</li>
  <li>encrypt</li>
  <li>encrypt_string</li>
  <li>rekey</li>
</ol>

## Create new encrypted Files

Let's create an encrypted file with ansible-vault.

To create an encrypted file we use the option `create` .

For example --> 

`ansible-vault create vault.yml`

You enter a password for the vault password and confirm this password then a code editor opens that allows you to write something to encrypt it.

Save this file and exit then you can see a new file created like `vault.yml` with encrypted data.

## Decrypt Files

For example we have an encrypted file and we want to decrypt it .

To decrypt files we use the option `decrypt` .

For example --> 

`ansible-vault decrypt vault.yml`

Then ask for your vault password to decrypt it.

So when you open this file we can see data that decrypted.

## View Encrypted Files

For example, you want to just see decrypted data and you didn't want to change the file (change encrypted file to decrypt).

In this case, you can use the option `view`.

For example --> 

`ansible-vault view vault.yml`

Then ask for your vault password to decrypt it and print it.

**in this case didn't change your encrypted file**.


## Encrypted Files

when you have a file and you want to encrypt this file and data.

In this case, you can use the option `encrypt`.

for example --> 

`echo "hello my name is Moein" >> greeting.txt`

`ansible-vault encrypt greeting.txt`

Then ask for your password and confirm it.

So you can see this message like `Encryption successful`.

If you open the `greeting.txt` file, this file is encrypted and has lots of numbers.

## Change the password of the encrypted file

We want to change the password of an encrypted file.

In this case, you can use the option `rekey`.

for example --> 

`ansible-vault rekey greeting.txt`

Then ask you `previous password` and `new password` and if you enter a the correct value , print this message `Rekey successful`.


----

[reference](https://www.digitalocean.com/community/tutorials/how-to-use-vault-to-protect-sensitive-ansible-data)
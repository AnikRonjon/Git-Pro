SSH keys are generated through a public key cryptographic algorithm,the most common being RSA or DSA
# Generate an SSH key using command line
- First execute the following to begin the key creation
```ssh-keygen -t rsa -b 4096 -C "your_email@example.com"```
This command will create a new SSH key using the email as a label
 

- You will then be prompted to "Enter a file in which to save the key." You can specify a file location or press “Enter” to accept the default file location.
```Enter a file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]```

- The next prompt will ask for a secure passphrase.
A passphrase will add an additional layer of security to the SSH and will be required anytime the SSH key is used. If someone gains access to the computer that private keys are stored on, they could also gain access to any system that uses that key. Adding a passphrase to keys will prevent this scenario.
```
> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]
```
At this point, a new SSH key will have been generated at the previously specified file path.

- Before adding the new SSH key to the ssh-agent first ensure the ssh-agent is running by executing:
```
$ eval "$(ssh-agent -s)"
> Agent pid 59566
```
- Once the ssh-agent is running the following command will add the new SSH key to the local SSH agent.
```
ssh-add ~/.ssh/id_rsa
```
- Copy the ssh key
```
clip < ~/.ssh/id_rsa.pub
```
> Now Go your github account > Settings > SSH and GPG keys > New SSH key and past it.

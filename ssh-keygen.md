SSH keys are generated through a public key cryptographic algorithm,the most common being RSA or DSA
# Generate an SSH key using command line
- First execute the following to begin the key creation
> `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
> This command will create a new SSH key using the email as a label
 

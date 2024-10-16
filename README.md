# Setting Up SSH for GitHub
Generate an SSH Key: If you don't already have an SSH key, you can generate one using the following command. 
Replace "your_email@example.com" with the email associated with your GitHub account.

```shell
ssh-keygen -t ed25519 -C "your_email@example.com"
```

# Step 2: Start the SSH Agent

```shell
eval "$(ssh-agent -s)"
```

# Add Your SSH Key to the SSH Agent: 
Add your newly created SSH key to the agent. 
If you used the default location, use:

```shell
ssh-add ~/.ssh/id_ed25519
```

Replace id_ed25519 with your key file name if you used a different name.

# Step 4: Copy Your SSH Public Key
You need to copy your SSH public key to add it to your GitHub account. Use this command:

```shell
cat ~/.ssh/id_ed25519.pub
```

This will display your public key in the terminal. Select the entire key and copy it.

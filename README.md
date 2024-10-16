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

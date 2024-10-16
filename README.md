# Setting Up SSH for GitHub
Generate an SSH Key: If you don't already have an SSH key, you can generate one using the following command. 
Replace "mne@yaposarl.ma" with the email associated with your GitHub account.

```shell
ssh-keygen -t ed25519 -C "mne@yaposarl.ma"
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

# Step 5: Add Your SSH Key to GitHub
Go to your GitHub account.
Navigate to Settings > SSH and GPG keys.
Click on New SSH key.
Paste your SSH key into the "Key" field and give it a title.
Click Add SSH key.

# Step 6: Test Your SSH Connection
To ensure everything is set up correctly, test your SSH connection:

```shell
ssh -T git@github.com
```

If everything is working, you should see a message like:
Hi username! You've successfully authenticated, but GitHub does not provide shell access.

# Step 7: Update Your Remote Repository URL
Finally, to use SSH with your existing repository, update the remote URL:

```shell
git remote set-url origin git@github.com:username/repository.git
```

Replace username and repository with your GitHub username and repository name.

Understanding the Process
Do you feel comfortable with each step? If anything seems unclear—like the purpose of the SSH key or how the SSH agent works—please let me know! It’s important to grasp these concepts to ensure a smooth experience with GitHub and version control.

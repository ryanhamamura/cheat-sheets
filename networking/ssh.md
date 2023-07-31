## SSH
### Generating a new SSH key
```sh 
ssh-keygen -t ed25519 -C "your_email@example.com"
```

### Adding SSH key to the ssh-agent
Ensure the ssh-agent is running.
```sh 
eval "$(ssh-agent -s)"
```

Add SSH private key to the ssh-agent. If you created the key with a different name, or if you are adding an existing key that has a different name, replace `id_ed25519` in the command with the name of your private key file. 
```sh 
ssh-add ~/.ssh/id_ed25519
```



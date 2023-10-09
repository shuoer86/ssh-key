Adding your SSH key to the ssh-agent
Before adding a new SSH key to the ssh-agent to manage your keys, you should have checked for existing SSH keys and generated a new SSH key.
If you have GitHub Desktop installed, you can use it to clone repositories and not deal with SSH keys.

In a new admin elevated terminal window (PowerShell or CMD), ensure the ssh-agent is running. You can use the "Auto-launching the ssh-agent" instructions in "Working with SSH key passphrases", or start it manually:

# start the ssh-agent in the background
Get-Service -Name ssh-agent | Set-Service -StartupType Manual
Start-Service ssh-agent
In a terminal window without elevated permissions, add your SSH private key to the ssh-agent. If you created your key with a different name, or if you are adding an existing key that has a different name, replace id_ed25519 in the command with the name of your private key file.

ssh-add C:\Users\YOU/.ssh/id_ed25519
Add the SSH public key to your account on GitHub. For more information, see "Adding a new SSH key to your GitHub account."

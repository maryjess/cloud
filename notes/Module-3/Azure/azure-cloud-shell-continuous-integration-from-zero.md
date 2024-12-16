# Azure Cloud Shell Continuous Integration from Zero

## Create Virtual Environment named `scaffold` in home directory
```
python3 -env venv ~/.scaffold
```

## Source the Venv to activate "that" version of Python
```
source ~/.scaffold/bin/activate
```

Terminal will now show smth like
```
(.scaffold) jessica $
```

## Create SSH Keys
```
ssh-keygen -t rsa
```
Then press enter a few times

### There are few things created when SSH key is created:
* ID should be saved in `/home/jessica/.ssh/id_rsa`
* Public key should be saved in `/home/jessica/.ssh/id_rsa.pub`
* Key Fingerprint
* Key's Randomart Image

Then, can see public key using `cat` command
```
cat /home/jessica/.ssh/id_rsa.pub
```

> Can work with any file too, it is a bash command

## Connect SSH Key to GitHub
1. Go to GitHub Profile > Settings > SSH and GPG Keys
2. Add new key
3. Title `azure-scaffold`
4. Key should be the one printed using `cat`

## Connect back the SSH Key from GitHub to Azure
```
git clone git@github.com:maryjess/scaffold.git
```

When prompted "Are you sure you want to continue connecting?", type `yes`


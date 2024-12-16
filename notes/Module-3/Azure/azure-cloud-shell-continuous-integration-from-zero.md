# Azure Cloud Shell Continuous Integration from Zero

Note: Connect with the Classic Azure Shell first before performing the below steps.
If not you'll have to start over the process, ugh.

## Create Virtual Environment named `scaffold` in home directory (if not already done so)
If virtual environment is already created, skip this step
```
python3 -env venv ~/.scaffold
```

## Source the Venv to activate "that" version of Python
```
source ~/.scaffold/bin/activate
```

Terminal will now show something like
```
(.scaffold) jessica $
```

## Create SSH Keys (if not already done so)
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

## Connect SSH Key to GitHub (if not already done so)
1. Go to GitHub Profile > Settings > SSH and GPG Keys
2. Add new key
3. Title `azure-scaffold`
4. Key should be the one printed using `cat`

## Clone the Scaffold Repo from Git (if not already done so)
```
git clone git@github.com:maryjess/scaffold.git
```

When prompted "Are you sure you want to continue connecting?", type `yes`

---

## Open the editor (the fifth or the `{}` icon)
in order to access the files

## Create new requirements file
(In the `scaffold/` dir)
```
touch requirements-azure.txt
```

## Modify Makefile
```
install:
	pip install --upgrade pip &&\
		pip install -r requirements.txt

install-azure: 
# command for azure, configured using requirements-azure.txt
	pip install --upgrade pip &&\
		pip install -r requirements-azure.txt
```

### How to run the Makefile?
In the terminal:
```
make (command)

# for instance:
make install-azure
make lint
```

Make sure that your terminal is currently in same directory as the Makefile

---
# After Editing Your Code

## Git Configuration (if not already done so)
If you're committing, then found this on the terminal:

```
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address 
```

Run this command:
```
git config --global user.email "youremail@email.com"
git config --global user.name "Jessica Listijo"
```

---

# Q&A

## In a Makefile, is there any command to make sure that ALL packages in requirements.txt meet the Python version being ran in the virtualenv?
* For instance, what if there are several (more than one, not just for instance `lint`) packages that are incompatible with say Python 3.5 -- so that we do not manually run `make <command>` one by one?
  * For `lint` itself, code can be made backward compatible by changing printf into prints syntax
    ```
    print(f"hello, {variable}")
    
    change to:
    
    print("hello, %variable" % variable)
    ```

## Divergent Git branches in Azure, how to reconcile?
Issue while pulling from origin
```
hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint: 
hint:   git config pull.rebase false  # merge
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only
hint: 
hint: You can replace "git config" with "git config --global" to set a default
hint: preference for all repositories. You can also pass --rebase, --no-rebase,
hint: or --ff-only on the command line to override the configured default per
hint: invocation.
```

Run this:
```
git config pull.rebase false 
# merge

git config pull.rebase true
# rebase

git config --global pull.ff only
# fast-forward only
# --global label is for all repo 
```
Home Assistant DevOps Flow

Development Node:

Install the extension 'Terminal + SSH'.
Once the extension is installed, enable it, and use it to open a session within your HAAS environment

## Create a SSH Keypair for working with GitHub
```sh
mkdir .ssh
ssh-keygen -t rsa -b 4094 -C "hass@deercrest.info"
```

* Save to `/root/config/.ssh/id_rsa`
* No passphrase

Now we have a credential we can use to communicate with GitHub, which we will use in a next stage

## Enable GIT

Currently our configuration is not versioned, we will initialize a starter repository in the `/config` folder, and connect it to our repository in GitHub

### Initialise GIT

> Before we run the next shell commands, first make sure you have placed in a `.gitignore` file in the `/config` folder so intstuct Git not to put sensitive data into the repo, reference the file I am using

Now, on the shell, execute the following commands

```sh
git init
git add -A :/
git commit -m "Getting Started"
git remote add origin git@github.com:damianflynn/home-assistant.git
git config core.sshCommand "ssh -i /root/config/.ssh/id_rsa -F /dev/null"
```

### Add Key to Github

Next, we will add the public key from the SSH keys, and put this into github. Start by printing to the console the public key and then copy that information to the clipboard

On the SSH Terminal, again type:

```sh
cat /ssh/id_rsa.pub
```

Now, Switch back to GitHub, where we have our repository:

* Open **Settings**, 
* Select the option **SSH anf GPG Keys**. 
* Now **Add New SSH** key
   * Paste in the public key from our clipboard, into the *key* section of the form, 
   * In the *title* provide a name that will help you recognise the credential, for example *Home Assistant*. 
   * Click the button **Add SSH Key**

### Push the to GitHub

Back in the Terminal, we can now push the current configurtaion to github, which should automatically authenticate with the SSH credentials we just provisioned and trusted

```sh
git push -u origin main
```


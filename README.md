Welcome to LiftForward. Hopefully the following guide will help you get your workstation setup. 

# 1. Setup your new workstation

 1. create a user etc on your mac
 1. use your own app store login
 1. Turn on the screensaver to require password when locked! very important

# 2. Install [Homebrew](https://brew.sh/)

run this to install homebrew on your new workstation
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

# 3. Clone this repo
  1. Create an access token for your machine [need instruction]
  1. Clone this repo with `git clone https://github.com/liftforward/new-developer-setup`
  1. Cd into this repo's working directory
  1. run `brew bundle` 
  
This should install some common tools (basically Slack and 1Password) we use for development 
which you'll neeed. You're free to install others and modify this as needed.

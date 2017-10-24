Welcome to LiftForward. Hopefully the following guide will help you get your workstation setup and deliver something into production. So far we have a 100% success rate of delivering to production on the first day. Don't let us down.

# 1. Setup your new workstation

 1. create a new user and stuff on your mac
 1. use your own app store login
 1. Turn on the screensaver to require password when locked! **very important**

# 2. Fork our dotfiles directory

 Fork the https://github.com/mikegrassotti/dotfiles project. If you already have a dotfiles repo we should chat about next steps. After forking take a look at it's brewfile. There may be some stuff you don't want installed or extra stuff you do. The script installs a number useful tools we strongly recommend as well as some things we require. 

You can also create an additional repo under your github account named `homebrew-brewfile` and add a single Brewfile. Our setup script will install these tools as well. 

# 3. strap https://github.com/MikeMcQuaid/strap

Strap is a setup script from github which will trigger your dotfiles and other things to setup your machine. To use is visit  https://macos-strap.herokuapp.com to generate a script custom to you and then run it:

 ```
 cd Downloads
 bash strap.sh
 rm strap.sh
 ```

Hopefully this all works fine and you can move onto setting up and installing all our projects.

# 4. Setup the API project
 1. follow the setup instruction here: https://github.com/liftforward/api
 
# 5. Setup the Ember projects: Lift, Lift-Admin, and Partner
 1. follow the setup instruction here: https://github.com/liftforward/lift
 1. follow the setup instruction here: https://github.com/liftforward/lift-admin
 1. follow the setup instruction here: https://github.com/liftforward/partner

# 6. Run through the user experiance once
You'll probably need help for this part so don't be afraid to ask.

 1. startup the api project `foreman start`
 1. startup the lift project `ember server --proxy=http://localhost:3000`
 1. visit the microsoft site and submit an application http://localhost:4300/microsoft/surfacemembership
 1. check your inbox for the emails the site generates
 1. start the admin project `ember server --proxy=http://localhost:3000`
 1. visit the admin site and approve your application http://localhost:4200
 1. check your inbox for the site emails
 1. return to the lift application and checkout
 1. check inbox for more emails
 1. return the admin site and fund your order
 1. no more emails 

# 7. Deliver something to production
 1. Get a task from someone
 2. Implement it on a branch
 3. Push branch and create PR
 4. Get PR approved
 5. Merge it
 6. Test in staging
 7. Release it using github releases feature with a tag version formated as release-YYYY-MM-DD-01
 8. Verify it works in production
 9. Go to fridge and have a beer your first day is over

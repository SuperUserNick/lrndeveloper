# lrndeveloper
A repo for developer tools to build lrn polymer elements even faster then stock as well as helping streamline installation issues associated with dependencies on your computer to do so. If you get any errors about permissions along the way you may need administrative permissions on your machine.

## How to use this from nothing
copy and paste the following and it'll do everything you need to get started as a lrn developer
`cd ~/ && mkdir -p Documents/git/elmsln/LRNWebComponents/ && cd Documents/git/elmsln/LRNWebComponents/ && curl -s https://api.github.com/orgs/LRNWebComponents/repos?per_page=200 | ruby -rubygems -e 'require "json"; JSON.load(STDIN.read).each { |repo| %x[git clone \"#{repo["html_url"]}\" ]}' && cd lrndeveloper`

### Install node
Go to https://nodejs.org/en/ and install the 6.x+ LTS release.

### (optional) I don't have polymer/bower/npm setup though
No problem, there's a one liner for that
`cd ~/Documents/git/elmsln/LRNWebComponents/lrndeveloper && sudo sh osx-setup.sh`

## shortcut for lrndev cli
To get the CLI in place type the following:
`echo "alias lrndev='bash ~/Documents/git/elmsln/LRNWebComponents/lrndeveloper/lrndev.sh'" >> ~/.bash_profile && source ~/.bash_profile`

Now you can run the CLI by typing `lrndev` from anywhere and step through the prompts.

After this, to build a new component for lrn type the following:
`cd ~/Documents/git/elmsln/LRNWebComponents/lrndeveloper/ && sh lrn.sh element-name` where element-name is the name of your new lrn element. This could be lrn-whatever, lrndesign-whatever, hax-whatever, or lrnsys-whatever. The point is that this will then
- Build a directory for this location by copying a boilerplate element
- rewrite everything to be the right name
- make a new git repo / put everything produced in version control
- do a polymer serve --open to give you a mini serve instance to see what it made

From here, it's your responsibility to build something awesome for education. Make us great!

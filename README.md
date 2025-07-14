A SHORT DESCRIPTION OF GIT AND GITHUB AND SETUP STEPS

WHAT IS VERSION CONTROL?: It is a track for changes and improvements made from 
the start to the finish of a project development.

IMPORTANCE OF VERSION CONTROL
version control helps to know the changes made to a file
its help to keep records of a working progress 
it helps keep track of time and date of when a change was made to a file

WHAT IS GIT?: Git is an open-source distributed version control system, A
tool which help developers track changes to their codes effortlessly overtime.

WHAT IS GITHUB?: GitHub is a collaborative platform that relies on GIT, which 
tracks changes to files over time, allowing developers to revert to previous
versions, compare changes and collaborate / contribute to an open-source
project as a team remotely.


DIFFERENCES BETWEEN GIT AND GITHUB

GIT                                     GITHUB
-----------------------------------------------------------------------------
free and open-source control tool   |   pay to use online servive built to run
for developers                      |   git in the cloud
                                    |
decentralized                       |   
-----------------------------------------------------------------------------


A COMPREHENSIVE GIT AND GITHUB SETUP GUIDE FOR BEGINNERS

Here i'll be explaining a step by step feature on hoe to configure your git and
github and make your first project push,
so lets say for a new user you should have your gthub account or if you dont have an
account create one here at https://github.com
so, you should have your github acc already
On your local machine go to your terminal and type in 
git --version this command shows your installed git version and if you dont have
git installed it will prompt you command git not found, not to worry use the following
command to install git to your pc <sudo apt-get install git> when you hit enter this
 will ask for your password to install, type and hit enter, now vheck your git version
again you should have git installed. lets configure git to our github profile
go to your terminal type in 
<git config --global user.name "your github user_name"> [replace "your github user_name"]
and hit enter
after that we the same with our mail 
<git config --global user.email "your github email"> [replace "your github email"] and 
hit enter
now check your added infos using <git config --list> enter
create an ssh key for your machine simply by entering thr command below
<ssh-keygen -t ed25519 -C "your github user email"> hit enter
run this command <eval "$(ssh-agent -s)">
run this command aswell <ssh-add ~/.ssh/id_ed25519> this adds your system as the current 
local machine via ssh
type in <cat ~/.ssh/id_ed25519.pub> to your terminal and enter this will concatinate your
ssh pubkey make sure to copy the while value catinated to the terminal
now head to your github account, click on the tiny profile like logo and click on settings
click on SSH and GPG keys
now lets click on new ssh and paste the ssh pubkey copied, it starts with 'ssh-rsa and ends with .com' now click on add ssh key 
congratulatons you have successfully configured your github to git!













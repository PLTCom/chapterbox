### Random notes
1) centOS8 minimal doesnt come with Python3, needs to be configured manually. May be a good first task for the installer.

#### update and upgrade server (bash script?)
Step 1) sudo dnf update && sudo dnf upgrade
Step 2) sudo dnf install python3

### Connect local ansible to remote
1) make sure Python3 is installed on remote machine
2) on LOCAL machine, make sure ansible is installed
3) download chapterbox repo to home directory
4) Set env variable ANSIBLE_CONFIG to $HOME/ansiblefiles/ansible.cfg
4) edit ansible.cfg to point default inventory to chapterbox

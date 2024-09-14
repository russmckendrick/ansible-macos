# Ansible macOS Deployment

My macOS setup using Ansible.

## Prerequisites

Install [Homebrew](https://brew.sh):

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Install Conda and Ansible:

```
brew install miniconda git
conda create -n ansible python=3.12
conda activate ansible
python -m pip install ansible
```

## Running

```
conda activate ansible
mkdir ~/Code/
cd ~/Code/
git clone https://github.com/russmckendrick/ansible-macos.git
cd ansible-macos
ansible-playbook -i inv main.yml --tags "home" # run if home machine
ansible-playbook -i inv main.yml --tags "work" # run if work machine
```
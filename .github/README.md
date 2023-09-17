
<p align="center">
    <img src="https://avatars.githubusercontent.com/u/1507452" width="100" />
    <h1 align="center">Ansible Playbooks</h1>
</p>

**My personal collection of Ansible Playbooks I use in my homelab and production environments.**

I have recently started to learn Ansible and I regret not trying it sooner! As it turns out, I have a fair amount of machines to manage and often end up peforming the same tasks on each one. To escape from the land of endless copy-pasting and bash scripts, I have created some playbooks that are useful for my use cases.

I am no expert when it comes to Ansible and I am still learning, so please do not expect anything on here to be done in the best way, although I will try my best to keep with reccomended practices.

---

## Setting Up
Assuming you don't have ansible installed, you should probably do so first on the machine you want to run the playbooks from.
```bash
# Install with Apt (Install sshpass to support SSH Passwords)
sudo apt -y install sshpass ansible

# Install with Pip
sudo pip3 install --upgrade pip
pip3 install ansible
```

Now let's clone the repo and create our inventory.
```bash
git clone https://github.com/SquashyTomato/Ansible-Playbooks
cd Ansible-Playbooks
touch inventory.ini
```

Now edit your Inventory file, you should follow the Ansible documentation to set this up. If you want to run any of these playbooks, use the same host group value in your config or change the playbook as needed.

---

## Things you should know
The Configuration file in this repo is designed for a Homelab Environment, so `host_key_checking` is turned off by default. Just change the value to `True` if you wish to enable it.

Also another quick reminder that I am no expert, I am still learning myself! By all means use these playbooks but any bugs/issues you may have are up to you to resolve. If you have spotted a bug and would like to open a PR then you are welcome to do so. :)

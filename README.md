# Patch vmware esxi with Ansible 

This repository contains ansible playbook for patching vmware esxi, text file for references, zip file for releases playbook

You can `cd` into any of the included directories and run ansible-playbook on it.

# Some examples to use this playbook.

## Prereq

  - **VMWARE ESXi 8** (`vmware esxi8` - as ansible target for patching, in this example with ip 10.11.8.87)
  - **linux server** (`linux server` - as ansible host for running playbook)
  - **patch files** (`patch files` -  already uploaded to vmware esxi server)

## Commands

```
git clone https://github.com/widansible/vmware-esxi-playbooks
cd VMWARE-ESXI-PATCH-PLAYBOOK
ansible-playbook -i 10.11.8.87, vmware-esxi-8-patch.yml --ask-pass
```

**Notes:**
- change or edit PATCH_FILE_PATH located at vars.yml to the path of your current patch file
- change or edit user with your desired user
- if you already put ssh public key to vmware esxi server, then you can remove the --ask-pass option 
```
ansible-playbook -i 10.11.8.87, vmware-esxi-8-patch.yml
```

**Update**
- change delay to 600 seconds or 10 minutes after reboot esxi server, because some branded server took longer for reboot.

## License

WID license.

## Author Information

Created in 2024 by [Widya Nugraha](https://www.indonesiadot.com/), author of [not yet create any books](https://not-yet-create-any-books.indonesiadot.com/),
inspired by [Jeff Geerling](https://www.jeffgeerling.com/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/).

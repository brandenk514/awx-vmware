# awx-vmware
Using Ansible and VMware to deploy and manage VMs, snapshots, and more!

## Getting Started

### In AWX
1. Create source control, make sure to use their respective credential types too
2. Create a project and point to your fork and branch
3. Create an inventory with the servers you would like to target
4. Create a Template and choose **Job Type** of `run` then select for inventory and project from the dropdowns. Set your playbook as well. You can set your execution environment if you want, but it shouldn't be required. 
5. In the template, set your credentials to log on to the servers (SSH keys recommended).
6. Save the template and **Launch** the job

### vCenter
1. Create a service account for the connection from vCenter to Ansible. You can use the *administrator@vsphere.local* for testing, but this should **not** be used in production environments
2. Create a set of VMware credentials inside VMware. Credentials -> Add -> Credential type -> VMware

### Variables
This variables are stored in the **Variables** field in the job template. The can be stored in a **vars** yaml file as well.

| Variable name | Description |
| ----------- | ----------- |
| cluster_name | The cluster in vCenter that this VM will be placed |
| folder_path | The folder in vCenter that this VM will be placed |
| vm_name | The name of the VM |
| datacenter_name | The datacenter in vCenter where this VM will be placed |
| datastore_name | The datastore in vCenter where this VM will be placed |
| template | The full folder path to the template for the VM to be created from |
| guest_domain | Domain for the VM |
| guest_dns_server1 | DNS server |
| guest_dns_server2 | DNS server |
| guest_domain_name1 | DNS search domain |
| guest_domain_name2 | DNS search domain |
| snap_name | The name of the snapshot to be taken | 

## Get Involved
I welcome your feedback and ideas! I do this in my spare time so responses may take a while. Thank you for your patience! 

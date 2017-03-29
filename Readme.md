Install Oracle VirtualBox

https://www.virtualbox.org/wiki/Downloads

Thiswill warn that there is a slight disruption in network during the installtion but I've not seen any major discconnection to my RDP and Putty session so guess it's ok to ignore the warning. 

Install Vagrant

https://www.vagrantup.com/downloads.html

After installtion it will ask to reboot the Laptop.

Clone the Git Repository into a Folder

C:\> git clone <this_repo>


Copy all the ansible modules or the modules that you want to test inside your VM. This ansible
directory will be mapped into your VM in /ansible mount point and we can run/test ansible from this location.

C:\> cd ansible; git clone <ansible-module-repo.git>

C:\> cd ../vagrant

Start the VM. This will build the VM, install ansible and map the repository inside the VM.

C:\> vagrant up hpe-ansible-1

C:\> vagrant ssh hpe-ansible-1

$(hpe-ansible-1:/home/vagrant) ansible --version

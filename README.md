# Integration of RedHat Ansible Automation Platform with ServiceNow (draft)
Steps involved 

1. Install Virtual box on Windows
2. 
3. Install RHEL 9 on Virtual box
   - add a new virtual machine on virtual box
      give name, folder path where you want to store your VM and ISO image of RHEL (note version I am using is rhel-9.2-x86_64-dvd.iso), check skip unattended installation
   - hardware - give around 8 GB ram (or minimal of 2 GB ram) and 4 CPUs (or min 2 CPUs)
   - virtual hard disk - select create a virtual hard disk now - 40GB
   - review and Finish
5. Install RedHat Ansible Automation Platform on RHEL
6. Install servicenow.itsm on RHEL

command to restart automation-controller-service 
> automation-controller-service restart
> authenticate
>
login to registry.redhat.io to get the execution environment
> podman login registry.redhat.io
  Username: {REGISTRY-SERVICE-ACCOUNT-USERNAME}
  Password: {REGISTRY-SERVICE-ACCOUNT-PASSWORD}
  Login Succeeded!

  podman pull registry.redhat.io/ansible-automation-platform-22/ee-supported-rhel8:1.0.0-344

  reference - https://catalog.redhat.com/software/containers/ansible-automation-platform-22/ee-supported-rhel8/6273a6fa7d19ffee88be59fa?container-tabs=gti&gti-tabs=red-hat-login


  https://www.ansible.com/blog/certified-collection-servicenow


  anisible-navigator run play.yaml -i inventory -m stdout 

  

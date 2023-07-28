# Integration of RedHat Ansible Automation Platform with ServiceNow (draft)
Steps involved 

1. Install Virtual box on Windows
2. Install RHEL 9 on Virtual box
3. Install RedHat Ansible Automation Platform on RHEL
4. Install servicenow.itsm on RHEL

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

  

## Ansible

Disclaimer: It requires some TLC and some possible manual steps stated. But automates the majority of the LHC setup

### 1. Update the var/s at the top of lhc.yml 

``` 
    # paths
    path_to_your_quantum_mechanic: '/Users/andre/Projects/Subatomic/quantum-mechanic'
    path_to_your_local_hadron_collider: '/Users/andre/Projects/Subatomic/local-hadron-collider'
    path_to_minishift_start_output_log: '/Users/andre/Projects/Subatomic/'

    # options are virtualbox or xhyve
    vm_driver: 'virtualbox'

    # resources to allocate (may require trial and error)
    cpus: "4"
    memory_MB: "7000"
    disk_size_GB: "25"

    # as per local hadron collider requirements
    ansible_version_to_be_greater_than: "2.5.0"

    # time in seconds to wait for minishift to download iso's and start (1800 = 30 minutes)
    minishift_startup_timeout_secs: 1800
 ```

### 2. To run LHC environment
```
ansible-playbook lhc.yml -K -v
```    

Note: you may need to run the above with sudo

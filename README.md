## Ansible

Disclosure: It requires some TLC and some possible manual steps stated. But automates the majority of the LHC setup

### 1. Update the var/s at the top of lhc.yml 

``` 
path_to_your_quantum_mechanic: '/Users/fong/Projects/Subatomic'
 ```

### 2. To run LHC environment
```
ansible-playbook lhc.yml -K -v
```    

Note: you may need to run the above with sudo
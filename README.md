# bubble-blueprint

Description
------------
 --> TODO

Installation
------------
[0] Make sure you comply with the requirements and Centos 7.2 is installed.

[1] Download and run the pre-install script:
```
source <(curl -L https://raw.githubusercontent.com/MissionCriticalCloud/bubble-blueprint/master/install.sh)
```

[2] Rename the user file `example.json` in `data_bag/users` to your username. Edit the contents of the file with your username and public ssh key.

[3] Start the chef-client run: 
```
sudo chef-client -z -r recipe[bubble]
```

[4] VPN/SSH to the ipaddress of your newly installed bubble.

Requirements
------------

#### Hardware
##### Minimal
- `CPU` Intel 4 core 64-bit processor with virtualization extensions
- `RAM` 16GB
- `HDD` 20GB

##### Recommended
- `CPU` Intel Skylake 4 core 64-bit processor with virtualization extensions
- `RAM` 32GB
- `SSD` 20GB (root) + 100GB (data)

#### OS
- Centos 7.2 `http://buildlogs.centos.org/rolling/7/isos/x86_64/CentOS-7-x86_64-Minimal.iso`

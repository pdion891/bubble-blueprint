# Bubble Blueprint

Description
------------
This installs a Bubble from scratch. You can create a Bubble using any computer that meets the requirements (see below). An Intel NUC for example works perfectly fine.

Installation
------------
Run this from the host you create The Bubble:

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

Run this from your laptop, to connect to The Bubble:

[4] Setup L2TP VPN connection to the ipaddress of your newly installed bubble.

![screen shot 2016-03-18 at 13 28 57](https://cloud.githubusercontent.com/assets/1630096/13877811/68585b16-ed0d-11e5-9790-15ad2702f5a2.png)

Bubble Toolkit
-------------
Scripts to work with The Bubble can be found here: https://github.com/MissionCriticalCloud/bubble-toolkit

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

License and Authors
-------------------
License: Apache Version 2.0
Authors: Fred Neubauer, Remi Bergsma, Bob van den Heuvel, Boris Schrijver, Miguel Ferreira, Wilder Rodrigues

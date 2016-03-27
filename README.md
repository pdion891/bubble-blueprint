# Bubble Blueprint

Description
------------
This installs a Bubble from scratch. You can create a Bubble using any computer that meets the requirements (see below). An Intel NUC for example works perfectly fine.

Installation
------------
Run this from the host you create The Bubble:

1. Make sure you have configured you SSH keys in both your github profile and the computer where you are cloning this repo.
2. Make sure you comply with the requirements and Centos 7.2 is installed.
3. Download and run the pre-install script:

   ```
   source <(curl -L https://raw.githubusercontent.com/MissionCriticalCloud/bubble-blueprint/master/install.sh)
   ```
4. Rename the user file `example.json` in `data_bag/users` to your username. Edit the contents of the file with your username and public ssh key.
5. Start the chef-client run:

   ```
   sudo chef-client -z -r recipe[bubble]
   ```

   Run this from your laptop, to connect to The Bubble:
6. Setup L2TP VPN connection to the ipaddress of your newly installed bubble.

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
Authors:
* Fred Neubauer
* Remi Bergsma
* Bob van den Heuvel
* Boris Schrijver
* Miguel Ferreira
* Wilder Rodrigues

```text
Copyright 2016, Schuberg Philis

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

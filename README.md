sa-denyhosts
============

Important: is is recommended to consider fail2ban utility alternative. Use denyhosts only if you really need it. Take a look on sa-box-bootstrap for example of usage.

DenyHosts is a python program that automatically blocks SSH attacks by adding entries to /etc/hosts.deny. DenyHosts might also inform Linux administrators about offending hosts, attacked users and suspicious logins.

[![Build Status](https://travis-ci.org/softasap/sa-denyhosts.svg?branch=master)](https://travis-ci.org/softasap/sa-denyhosts)


Example of use: check box-example

Simple:

```YAML


     - {
         role: "sa-denyhosts"
       }

```


Advanced:

```YAML

my_whitelisted_boxes:
  - "sshd:	192.168.0.10"
  - "sshd:	192.168.0."
  - "sshd:	192.168.0.0/255.255.255.0"

```

```YAML


     - {
         role: "sa-denyhosts",
         deploy_whitelisted_hosts: "{{my_whitelisted_boxes}}"
       }

```


Copyright and license
---------------------


Code licensed under the [BSD 3 clause] (https://opensource.org/licenses/BSD-3-Clause) or the [MIT License] (http://opensource.org/licenses/MIT).

Subscribe for roles updates at [FB] (https://www.facebook.com/SoftAsap/)

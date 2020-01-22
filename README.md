
Automate download, modification and write of raspberry pi OS images with this ansible playbooks.

# Usage

* copy "host_vars/localhost.example" to "host_vars/localhost"
* edit settings in "host_vars/localhost"
* run playbooks...
  * ...to build vanilla OS image: ```ansible-playbook sdcard-vanilla.yml```
  * ...to build minimal image with sane settings: ```ansible-playbook sdcard-minimal.yml```
  * ...

You will be asked for a sudo password since probing partitions and writing to
the OS image on a loopback mount requires root.

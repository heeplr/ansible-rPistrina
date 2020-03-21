
# Generating raspberry pi images has never been simpler

Automated downloading, modification and SD card writing of raspberry pi OS images using ansible playbooks.

## Usage

* copy "host_vars/localhost.example" to "host_vars/localhost"
* edit/add settings in "host_vars/localhost"
* run playbooks...
  * ...to build vanilla OS image: ```ansible-playbook sdcard-vanilla.yml```
  * ...to build minimal image with sane settings: ```ansible-playbook sdcard-minimal.yml```
  * ...

You will be asked for a sudo password since probing partitions and writing to
the OS image on a loopback mount requires root.

By default the OS image will just be created, not written to the sdcard. If
you like to write the image, set ```sdcard_burn: yes``` and
```sdcard_dev: /dev/sdX``` to point to your SD card.

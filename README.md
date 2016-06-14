# ansible-opendaylight

This is a simple, as simple as I could make it really, ansible role to deploy an OpenDaylight controller.

## Variables

The defaults/main.yml file has some default variables set, most specifically the base URL to download the Opendaylight tar file, as well as the tar file's actual name. Please set those to what version you would like.

There is also an opendaylight_karaf_features variable. Right now it's setup to work with an OpenStack deployment. That might not be what you want, so ensure to override that variable with the required karaf features for your particular deployment.

## Example playbook

```
---

- hosts: odl
  roles:
    - ansible-opendaylight
```

## Notes

Please note that the Opendaylight tar file is rather large, almost 300MB so it will take a while to download. This also presumes the host can download the file from the internet.

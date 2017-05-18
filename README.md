# Ansible Role: dcm4chee2

Install
[dcm4chee-2.x DICOM Clinical Data Manager system](https://dcm4che.atlassian.net/wiki/display/ee2/)
on Ubuntu Linux.

**NOTE: Alpha release / Work in progress!**

## Requirements

None.

## Role Variables

### Storage directory

dcm4chee stores by default all DICOM files into
`{{ dcm4chee2_home }}/server/default/archive`.
If you define `dcm4chee2_storage` then the default location will be symlinked
to this directory (needs to be present and writable by system-user "dcm4chee"):
Example:

```yaml
dcm4chee2_storage: "/mnt/storage/dicom"
```

By that you can keep your data on a bigger storage.


## Dependencies

None.

## Example Playbook

```yaml
- hosts: pacs
  roles:
     - { role: bjoernalbers.dcm4chee2 }
```

## License

This Ansible role is released under the [MIT License](LICENSE.txt).

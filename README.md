# A Packer test build

Headless for VMWare Player not working.

This fails for me:

    HEADLESS=true packer build test.json

This works for me:

    HEADLESS=false packer build test.json

The build error (but it seems vmware logs are cleaned up):

```
Build 'vmware-centos6' errored: Error starting VM: VMware error: Error: Unknown error

Packer detected a VMware 'Unknown Error'. Unfortunately VMware
often has extremely vague error messages such as this and Packer
itself can't do much about that. Please check the vmware.log files
created by VMware when a VM is started (in the directory of the
vmx file), which often contains more detailed error information.

==> Some builds didn't complete successfully and had errors:
--> vmware-centos6: Error starting VM: VMware error: Error: Unknown error

Packer detected a VMware 'Unknown Error'. Unfortunately VMware
often has extremely vague error messages such as this and Packer
itself can't do much about that. Please check the vmware.log files
created by VMware when a VM is started (in the directory of the
vmx file), which often contains more detailed error information.

==> Builds finished but no artifacts were created.
```

System:
 UbuntuGnome: 16.10
 packer: 0.12.2
 vmware-player: 12.5.1.4542065      
 vmware-vix: 1.11.2.591240

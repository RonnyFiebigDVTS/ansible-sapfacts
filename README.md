# ansible-sapfacts

This GitHub Repository provides an improved Version of the orginal sapfacts.sh from the community.sap_operations Ansible Collection ![[assets/13245039dccf3f6ea39129bdc31c4774_MD5.svg]]
  
My aim was to utilise further information from an SAP system in order to use it for real SAP operations scenarios such as a kernel swap, the exchange of certificates or simply for parameter maintenance.

## Functionality

The version of the provided script can be exchanged 1 to 1 with the original script. It offers all previously available functions and extends them with the following:  

| Function               | Purpose                                                           | Output Example |
| ---------------------- | ----------------------------------------------------------------- | -------------- |
| get_sap_kernel_release | Provides the SAP kernel release of the SAP system                 | "789"          |
| get_sap_kernel_version | Provides the SAP kernel version of the SAP system                 | "1039"         |
| get_sap_kernel_os_type | Provides the SAP kernel Operating System Type of the SAP system   | "linuxx86_64"  |
| get_sap_kernel_db_type | Indicates the type of database on which the SAP system is running | "hdb" or "syb" |
| get_sap_unicode_status                       | Indicates the Unicode Status of the system                                                                  |  "uc"              |

## Output example

```
{
    "InstanceNumber": "10",
    "InstanceType": "SCS",
    "Kernel OS Type": "linuxx86_64",
    "Kernel Release": "753",
    "Kernel Version": "1100",
    "SID": "SMJ",
    "Type": "nw",
    "Unicode Status:": "uc",
    "Used DB:": "hdb"
}
```

## Requirements, Dependencies and Testing

### Operating System requirements

Like the original script and as indicated by the file extension, it is only developed for Linux systems such as RHEL or SUSE. It has not yet been tested on AIX.
### Testing on target/remote host

**SAP Components**

- SAP Netweaver 7.40 and 7.50 AS ABAP including ERP 6 EHP 7 and 8
- SAP Solution Manager 7.2 (ABAP and JAVA)
- SAP HANA 2.0
- SAP Process Orchestration (AS JAVA)

**Operating System**

- SLES (for SAP) 12.5
- SLES (for SAP) 15.x
- RHEL 8.2 for SAP

## License

- [Apache 2.0](./LICENSE)
## Contributors

Contributors to the Script, are shown within [contributors](.CONTRIBUTORS.md).
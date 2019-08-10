# Filesystem

### Add filesystem configuration details to _systemdescription.yaml_

sample yaml snippet

```yaml
fs1::LOCAL: !<FileSystemSettings>
    directories:
      - path: C:\drift-file-system-test\root-folder-1
      - path: C:\drift-file-system-test\root-folder-2

```

### Testing the connection settings

You can verify the connection settings in the "System Connections" page by clicking "Test" button.

![](../../../.gitbook/assets/systemconnections-0.0.3.png)


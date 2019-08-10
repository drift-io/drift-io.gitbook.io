# Configuration

The _systemdescription.yaml_ file is located in directory store/system  

This file contains following sample  content

```yaml
---

subSystems:
  - key: PETSDB
    type: jdbc
    name: Pets Database
  - key: PRODUCTSDB
    type: jdbc
    name: Product Catalog
  - key: fs1
    type: filesystem
    name: 'Drive C:'

environments:
  - key: LOCAL
    name: Local
  - key: DEV
    name: Develop

connectionDetails:

  PETSDB::LOCAL: !<JDBCConnectionDetails>

    userName: user1
    password: pwd
    jdbcUrl: jdbc:h2:tcp://localhost/./test

    tableNames:
      - OWNERS
      - PETS
      - VETS

  PRODUCTSDB::LOCAL: !<JDBCConnectionDetails>

    userName: user1
    password: pwd
    jdbcUrl: jdbc:h2:tcp://localhost/./test2

    tableNames:
      - CUSTOMER
      - PRODUCT
      - SUPPLIER

  fs1::LOCAL: !<FileSystemSettings>
    directories:
      - path: C:\drift-file-system-test\root-folder-1
      - path: C:\drift-file-system-test\root-folder-2

```

The file has 3 sections:

* subsystems: 
  * a list subsystem descriptions
  * every subsystem has

    * key: unique id of the subsystem
    * type: 
      * 'jdbc' for SQL database subsystem
      * 'filesystem' for a file system
    * description
* environments
  * a list of environments \(e.g. LOCAL, DEVELOPMENT, STAGING, PROD...\)
  * every subsystem has a 

    * key: unique id of the environment
    * description 
* connectionDetails
  * a map of subsystem specific connection details for each subsystem/env combination
  * key: combination of &lt;subsystem key&gt;::&lt;environment key&gt;
  * value: subsystem specific connection details
    * jdbc: see [JDBC Connections](jdbc-connections.md)
    * filesystem: see [Filesysystem](filesystem.md)




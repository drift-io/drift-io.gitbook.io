# Installation

See the [**release notes**](../release-notes.md) to see what's in each release and [**download**](https://github.com/driftserver/drift-server/releases) ****the release of your choice.

**unzip** into a folder of your choice. You should see following unzipped folder structure :

|  |  |
| :--- | :--- |
| │    _drift-server-&lt;release&gt;.jar_ | runnable jar with packaged drift server application |
| │    _run.bat_ | start script |
| ├─ **lib** |  extra jars to add to classpath, e.g. jdbc drivers |
| ├─ **store** | data dir |
|       ├── **index** | Lucene index dir |
|       ├── **recordings** | recordings data dir  |
|       └── **system**                                           | system data dir |
|                       _systemdescription.yaml_ | system description yaml file |
|  |  |




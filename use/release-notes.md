# Release Notes

## 0.0.2 - 2019-07-29

### Added

* Software Stack setup
  * Spring boot
  * Wicket + Bootstrap
  * Lucene
  * Plugin system
* System Description page
  * list system components, environments
* System Connectivity page
  * display connection parameters for each subsystem 
  * test connection settings per environment
* Recordings page  
  * list recordings with metadata
  * create a new recording
  * select existing recording
* recording page 
  * take snapshot
  * view snapshot details and deltas
* jdbc plugin
  * use Hikari connection pool
  * connectivity page contribution: 
    * display jdbc connection parameters
    * test jdbc connection
  * recording page contribution:
    * create and display jdbc snapshots and deltas

## 0.0.3 - 2019-08-10

### New features

* filesystem plugin
  * use apache commons file tracker
  * connectivity  page contribution:
    * display tracked directories
    * test existence of tracked directories
  * recording page contribution:
    * create and display file system snapshots and deltas

### Bug fixes

* FIXED: "DB delta contains unchanged rows as rows of type "U" when a table  has no PK or a PK without colums"

### Enhancements

* DB delta: updated row displays old value \(striked through and in red\) next to new value


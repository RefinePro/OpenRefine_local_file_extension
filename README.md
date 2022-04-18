
## Description

OpenRefine extension to load CSV files from a local environment. Compatible with OpenRefine 3.3
Default location is the `Download` folder from the home user directory.

## Requirements

* Java 1.8.*
* Maven 3.* (mvn)

## Compile

* Execute `mvn package assembly:single`
* Extension will be located into `target/local-file-system-1.0.2.zip`

## Installation

* Extract the `local-file-system-1.0.2.zip` into the OpenRefine folder `webapp/extensions`
* Run OpenRefine and you can start a new project form the `Workspace Data` tab

### Configure default location folder

* In the OpenRefine installation folder locate file `refine.ini`
* Open file and add the environment variable `EXT_LOCAL_FILE_SYSTEM` with the folder location value. Example: `EXT_LOCAL_FILE_SYSTEM=/data/files`
  * For Windows OS use the `refine.bat` to start OpenRefine, additional configuration in `refine.ini` won't be loaded using the `openrefine.exe` executable. Example `EXT_LOCAL_FILE_SYSTEM=C:\\Users\\Home\\Desktop`
* Another option is add the environment variable to any Shell script that start OpenRefine. Example: `export EXT_LOCAL_FILE_SYSTEM=/data/files`
**Note:** If you don't see any files from the defined location verify that the folder is a valid location in your environment and files are with valid READ permissions.


## Demo with Docker

* Use the docker image from [RefinePro/OpenRefine_Docker ](https://github.com/RefinePro/OpenRefine_Docker)

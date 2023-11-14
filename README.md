# Folder-Synchronization

#### This program performs one way synchronization of two folders(source and replica)
* The synchronization is one-way: after the synchronization content of the replica folder is modified to exactly match content of the source folder;
* Synchronization is performed periodically;
* File creation/copying/removal operations are logged into a file and to the console output;
* Folder paths, synchronization interval and log file path can be provided using the command line arguments;
* The script uses the MD5 hash of files to compare and determine if a file needs to be updated in the replica folder;
* If the replica folder does not exist, the script will create it;
* If the source folder does not exist, the script will raise an error;
* To stop the program manualy, press CTRL+C.

## Requirements
* Python 3.0 or higher;
* Libraries: hashlib, os, time, shutil, argparse, logging.

## How to use

```
python main.py --source source --replica replica --log-file log_file --time-interval time_interval
```

- `--source`: Path to the source folder that needs to be synchronized (default: "source");
- `--replica`: Path to the replica folder that will be updated to match the contents of the source folder (default: "replica");
- `--log-file`: Path to the log file (default: "log.txt");
- `--time-interval`: Time interval for synchronization in seconds (default: 10).

## Example

Perform one-way synchronization from the folder "project_source" to the folder "project_replica" and log the process to "project_synch.txt". Perform the synchronization process every 20 seconds.
Run the following comand:

```
python main.py --source project_source --replica project_replica --log-file project_synch.txt --time-interval 20
```

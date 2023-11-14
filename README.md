# Folder-Synchronization

#### This program performs one way synchronization of two folders(source and replica)
* The synchronization is one-way: after the synchronization content of the replica folder is modified to exactly match content of the source folder;
* Synchronization is performed periodically;
* File creation/copying/removal operations are logged into a file and to the console output;
* Folder paths, synchronization interval and log file path can be provided using the command line arguments.

## Requirements
* Python 3.0 or higher;
* Libraries: hashlib, os, time, shutil, argparse, logging.

## How to use

```
python main.py --source source --replica replica --log-file log_file --time-interval time_interval
```

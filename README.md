This is an extension for Drive Badger. It provides `exclude.list` file, containing a list of exclusions compatible with popular `rsync` program.

The purpose of these exclusions is to decrease the amount of data to be exfiltrated by Drive Badger, and thus to speed up the attack,
by eliminating files and directories, that are not valuable in any way to the attacker:

- multimedia files (avi/mkv/rmvb movies, mp3/flac music - except for game content)
- image files containing encrypted filesystems
- Mozilla Firefox/Thunderbird caches
- Windows memory dumps
- Windows search telemetry

### Installing

Clone this repository as `/opt/drivebadger/config/exclude-user` directory on your Drive Badger persistent partition.

### FAQ

Q: Why `avi`/`mkv`/`rmvb` movies are excluded from exfiltration, while `3gp`/`flv`/`mp4`/`webm`/`wmv` not?

A: Movies with `3gp`/`flv`/`mp4`/`webm`/`wmv` extensions are often user-generated content (by photo cameras, phones etc.), while `avi`/`mkv`/`rmvb` files
are considered "external movies" (eg. downloaded commercial movies) - usually very big, and not valuable at the same time. You can change this behavior:

- by forking this repository and cloning your fork instead of the original one
- by making a local change directly on Drive Badger USB device


### More information

- [Drive Badger main repository](https://github.com/drivebadger/drivebadger)
- [Drive Badger wiki](https://github.com/drivebadger/drivebadger/wiki)
- [description, how configuration repositories work](https://github.com/drivebadger/drivebadger/wiki/Configuration-repositories)

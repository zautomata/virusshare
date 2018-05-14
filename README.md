# Synopsis

virusshare.sh is a shell script collection for downloading malwares torrent archives from virusshare.com

## Technical Freatures
- [x] Ability to download a virusshare.com full torrent list 
- [x] Ability to check for virushare.com torrent archive updates 
- [x] Ability to store torrent meta information
- [x] Ability to interact with virusshare.com from terminal with secure access credentials
- [x] Ability download torrent contents via transmission-daemon(1)
- [x] Ability to manage torrents downloading via transmission-remote(1)
- [x] Ability to extract torrent contents upon download completion 
- [x] Ability to get snapshots of virusshare.com. 

## Usage
The user experience run a command, it will check for updates, download them and the torrent client will watch the torrent dir, and automatically load them on pause. then the user can choose which torrent to download. after that a script will automatically be executed once the torrent is completed and it will extract the malware.zip with "infected" password. (and possibly notify other programs that want to use it)

Alternativly you can control the downloads via transmissions web interface by visiting
`http://localhost:9091/transmission/web/` on your local machine. TransmissionWeb uses the same RPC mechanism of transmission clients.

To make virusshare scripts executable everywhere, add each script to the $PATH enviroment variable, i.e. `export PATH=$PATH:</path/to/virusshare> >> ~/.profile`

For a daily update crontab(1) maybe used i.e. `crontab -e` and adding `0 0 * * * virusshare` to run every midnight.

## Sample Hierarchy
```
.
|-- DATA
|   |-- 1.torrent.added (desc)
|   |-- 2.torrent.added
|   |-- 3.torrent.added
|   |-- 4.torrent.added
|   |-- 5.torrent.added
|   |-- 6.torrent.added
|   |-- 7.torrent.added
|   |-- VirusShare_00000.zip.part (desc)
|   |-- VirusShare_00001.zip.part
|   |-- VirusShare_00003.zip.part
|   |-- VirusShare_00004.zip.part
|   |-- VirusShare_00005.zip.part
|   |-- VirusShare_00006.zip.part
|   `-- torrent.list (desc)
|-- README.md **This file**
|-- logs
|   `-- transmission.log (desc)
|-- snapshots (desc)
|-- virusshare (desc)
|-- vsaddinfo (desc)
|-- vscheckupdates (desc)
|-- vscleanup (desc)
|-- vsdownload (desc)
|-- vssnap (desc)
`-- vstorrentfiles (desc)
```
# Installation
Create a sperate user account for the script to run
It is adivsed to run the virusshare on its own account.

give permission 0755 (or rwxr-xr-x) for the script 

## Dependencies
`sudo apt-get install transmission-cli transmission-daemon`

# Configuration
TODO

# Logging
TODO
# Further Information
TODO

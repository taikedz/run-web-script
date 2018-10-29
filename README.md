# Run Web Script

You know when a site says something along the lines of the following

> to use our project, run `curl http://oursite.net/script.sh | sudo bash`

that you should really be checking that script for content and tampering.

This project seeks to help alleviate that.

Instead of the above, you would run this:

    websh --sudo -s bash http://oursite.net/script.sh

`websh` takes care of downloading the script and checking its hash against an online database of hashes, or against a sidecar hash file, optionally with a signature

## Features

* download and hash script before running
* match URL to hash
* check for sidecar hash file
* centrally report URL+hash pairs to server
* retrieve counts of hashes per URL

# LANscape
A python based local network scanner.

![screenshot](https://github.com/mdennis281/py-lanscape/raw/main/src/lanscape/static/img/readme1.png)

## Local Run
```sh
pip install lanscape
python -m lanscape
```

## Flags
 - `--port <port number>` port of the flask app (default: 5001)
 - `--nogui` run in web mode (default: false)
 - `--debug` verbose logging (default: false)
 - `--logfile` save log output to lanscape.log
 - `--loglevel <level>` set the logger's log level (Default: INFO)

Examples:
```shell
python -m lanscape --debug
python -m lanscape --nogui --port 5002
python -m lanscape --logfile --loglevel DEBUG
```

## Troubleshooting

### MAC Address / Manufacturer is inaccurate/unknown
The program does an ARP lookup to determine the MAC address. This lookup
can sometimes require admin-level permissions to retrieve accurate results.
*Try elevating your shell before execution.*

### Unable to see results after initiating a scan
In order to keep this program lightweight and compatible, it leverages the filesystem to temporarily save the results of an active scan. Ensure that you have write permissions in the current working directory of your shell.

### Something else
Feel free to submit a github issue detailing your experience.



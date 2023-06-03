1) Install the following dependencies.
The generated script includes the following dependencies:
    • nmap: Python library that provides access to the nmap network scanner via code.
    • subprocess: Built-in module that allows to create new processes, connect to their input/output/error pipes, and obtain their return codes.
    • pyshark: Python library that allows to parse network packets captured by Wireshark/TShark using the Sharkd protocol.
    • binascii: Built-in module which provides a set of functions for converting between binary data and various string representations of it, such as hexadecimal or Base64-encoded.
    • PrettyTable: Third-party library that allows to create ASCII tables in a visually appealing way.
    • re: Built-in module that provides regular expression matching operations.
    • base64: Built-in module that provides functions for encoding binary data into ASCII strings using Base64 encoding.
    • paramiko: Third-party library which implements the SSH protocol and allows to establish SSH connections via code.
    • Beautifulsoup4 (bs4): Third-party library which allows to parse HTML and XML documents and extract useful information from them.
    • requests: Third-party library which allows to send HTTP requests and handle their responses.
    • argparse: Built-in module which provides an easy way to specify and parse command-line arguments.
    • csv: Built-in module which provides functions for working with CSV (Comma-Separated Values) files.
    • sys: Built-in module which provides access to some variables used or maintained by the interpreter and to functions that interact strongly with the interpreter.

2) Type "python3 Downloads/Exploit.py -ip 10.200.14.121 --help" for the options our Code provides.
[usage: Exploit.py [-h] -ip IPADDRESS [-d DIR] [-o OUTPUT]

Hacking Hero, Capture The Flag

options:
  -h, --help            show this help message and exit
  -ip IPADDRESS, --IPAddress IPADDRESS
                        Pass the hostname or IP to run scan
  -d DIR, --dir DIR     Provide the hidden path for flag2
  -o OUTPUT, --output OUTPUT
                        Provide the path of the Output CSV file.
]

3) To launch the attack and get the flags : 
For executing the script the below command has been used:
sudo python3 Exploit.py -ip 10.200.14.121 -d login


4) Open output.csv to view all the flags

5) Open msf.pcap and give display filter "ip.src==10.200.14.121 && tls.heartbeat_message" and check out the heartbeat responses. One of them has the password.

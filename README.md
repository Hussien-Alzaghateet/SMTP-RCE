
### Description 
-------
This code exploits improper input sanitization in SMTP headers to achieve Remote Code Execution (RCE) by injecting malicious commands into crafted email fields.


![[SMTP-RCE.png]]

### Requirements
---
```
sudo python3 -m pip install pwntools
```

### Installation 
--------
```
git clone https://github.com/Hussien-Alzaghateet/SMTP-RCE
```


# Usage
-----------
1. Start a listener on your machine to capture the reverse shell.
```
nc -lvnp 4444
```


2. Edit the Script 
- `target_ip`: Replace with the IP address of the target SMTP server.
- `listener_ip`: Replace with the IP address of your listener machine (the one running `nc`).
- `listener_port`: Ensure it matches the port used in your `nc` listener.
- `HELO`: Change the hostname in the line with `HELO` to the correct mail server hostname (if required).
- `RCPT TO`: Update the target email address to one that exists on the mail server.

3. Run the Script
```
python3 exploit.py
```
# SMTP-RCE

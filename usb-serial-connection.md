##Serial to USB On OpenBSD 

To connect one of those neat usb to serial convertors for console access to your switch, console, etc. 

mine is (tbd...) and shows up in dmesg like so

uplcom0 at uhub0 port 12 configuration 1 interface 0 "Prolific Technology Inc. USB-Serial Controller D" rev 1.10/4.00 addr 5
ucom0 at uplcom0

(as root?)

We'll use [cu(1)](http://man.openbsd.org/OpenBSD-current/man1/cu.1) since it's in base already.
```bash
cu -d -s9600 -lcuaU0
```
press **Enter** to get a prompt

Do your dirty work.  

To exit cu type

```bash
~.
```

That's it!



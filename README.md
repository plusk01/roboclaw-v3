RoboClaw v3
===========

RoboClaw v5 library ported to v3.1.9 (checksum instead of CRC)

To install and use:

```bash
$ pip install git+https://github.com/plusk01/roboclaw-v3.git@v1.0
```

**Note:** If you are using v3 firmware (which does not return a response) then be aware of the verify checksum option in `Open()`:

```bash
$ r.Open('/dev/ttySAC0',38400,verifyChecksum=False)
```

By default, `verifyChecksum` is set to `False`. This is to prevent the serial port from timing out waiting for a response that it will never get. (The serial port was set to timeout after 100ms of no response)

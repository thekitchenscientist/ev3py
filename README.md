ev3py
=====

This module implements the class 'ev3', which you can use to interact with LEGO Mindstorms EV3 bricks. The 'ev3' class communicates with the EV3's native firmware, so there is no need to create a bootable SD card; just turn on the EV3 and start coding.

For now the module is still inchoate; it only covers two basic functions (starting motors and reading data from sensors) and it only works on Macs, and only via Bluetooth. The goal is to eventually cover all EV3 capability and make ev3py work with USB and WiFi and also with Linux and Windows.

No installation is necessary. Just download the two files (ev3py.py and dec_to_hex.py) and import the ev3 class from ev3py.

Usage example:

    from ev3py import ev3

    mybrick = ev3()
    mybrick.connect('bt')
    mybrick.start_motor(port = 'a', power = 20)
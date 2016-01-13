OpenWRT Scripts
===============

Console
-------

Add to the bottom of `/etc/profile`:

    export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/tmp/libopenssl/usr/lib
    export PATH=$PATH:/tmp/openvpn/usr/sbin

Finally install dependencies and enable startup-script:

    opkg install liblzo kmod-tun
    chmod +x /etc/init.d/openvpn
    /etc/init.d/openvpn enable

Web-Interface
-------------

    1. Create VPN(tun0) interface
    2. Add VPN to WAN (firewall)
    3. Reboot

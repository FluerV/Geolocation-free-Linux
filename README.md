# Geolocation-free-Linux
How to remove geolocation from linux

I liked Gnome but recently i found that there is no way to complitelly delete geoclue (geolocation) from there because of dependencies.
I removed geoclue package but couldn't remove libgeoclue and Geoclue.typelib (it caused Gnome crash). Other programms can use libgeoclue to access your geolocation. 

If your wish to avoid any geolocation packages in your machine you can do this steps:

1.  Make fresh install with only XFCE (without print server and standart system utilities with nfs etc).
2.  Remove geoip package:
    a)apt purge geoip
    b)apt autoremove
    c)apt clean
    d)systemctl daemon-reload
    systemctl reset-failed

Optional
You can delete bluetooth also and make your OS more secure. 

apt purge bluez*
(steps 2.b, 2.c, 2.d)

Hope it helps make your life more safe! 

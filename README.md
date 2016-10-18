# Droid Module: timezone

Reconfigure the tzdata platform package to set the time zone. For more
information on Droid, please see [droidphp.com](http://droidphp.com).

The steps involved are:-

1. Copy a templated file containing the debconf selections required to
   configure the tzdata package with the desired time zone.
2. Insert the aforementioned selections into the debconf database.
3. Remove existing time zone configuration files.
4. Execute dpkg-reconfigure.


## Assumptions

1. The platform is Debian-based.
2. The tzdata package is already installed.


## Limitations

None.


## Information required by the module

1. One or more Inventory Hosts, having a `public_ip`.
2. Values for the following variables:-

        timezone:
          area: <string>  # for example, "Europe"
          zone: <string>  # for example, "Amsterdam"


## Optional information

None.

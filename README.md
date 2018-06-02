# Meraki Updater

![Language][python3] ![Language][python2]

![Issues][issues] ![Forks][forks] ![Stars][stars]

![License][license]

Bulk updates for your dashboard devices
-------
[![Tweet][tweet]][repo-tweet] [![Follow][follow]][twitter] [![Donate][paypal-badge]][paypal]

Update Meraki devices in a network using the provisioning API. Any information in the CSV will overwrite the dashboard values (including tags) so anything that should not be updated should be empty as shown in the example file. The CSV file should have the following columns: serial,name,tags,lat,lng,address.

Usage
------

######  Update devices in a single network from CSV:

        meraki-updater.py -k <MERAKI-PROVISIONING-API-KEY> -f <CSV-UPDATE-FILE>

######  Update devices from a CSV with network specified per device:

        meraki-updater.py -k <MERAKI-PROVISIONING-API-KEY> -m -f <CSV-UPDATE-FILE>

######  Write all devices on all accessible networks to a CSV (This file WILL be overwritten):

        meraki-updater.py -k <MERAKI-PROVISIONING-API-KEY> -g -o <CSV-OUTPUT-FILE>

######  Arguments:

        -k/--key            Set the Meraki Provisioning API key (required)
        -f/--file           Set the CSV file to read for device updates
        -o/--output         Set the CSV file to write network devices (This file WILL be overwritten)
        -g/--get            Get network devices from all networks and write them to CSV
        -m/--multinetwork   Update devices across multiple networks using a CSV
        -v/--ver/--version  Display the version of this script

About
------

###### Author: [Ryan M. Adzima][li]
###### Twitter: [@radzima][twitter]
###### Website: [Two Evil Geniuses][website]

License
------
###### GNU General Public License v3.0

###### See [LICENSE][license_file] to see the full text.


Donate
------
###### Like what you see? Want more? [Donate!][paypal]

[issues]: https://img.shields.io/github/issues/ryanadzima/meraki-updater.svg?style=flat-square "Issues"
[forks]: https://img.shields.io/github/forks/ryanadzima/meraki-updater.svg?style=flat-square "Forks"
[stars]: https://img.shields.io/github/stars/ryanadzima/meraki-updater.svg?style=flat-square "Stars"
[license]: https://img.shields.io/github/license/ryanadzima/meraki-updater.svg?style=flat-square "License"
[python3]: https://img.shields.io/badge/language-Python%203.4%2b-yellow.svg?style=flat-square "Language"
[python2]: https://img.shields.io/badge/language-Python%202.7%2b-yellow.svg?style=flat-square "Language"
[tweet]: https://img.shields.io/twitter/url/https/github.com/ryanadzima/meraki-updater.svg?style=social
[repo-tweet]: https://twitter.com/intent/tweet?text=Wow:&url=https%3A%2F%2Fgithub.com%2Fryanadzima%2Fmeraki-updater "Tweet this repo"
[follow]: https://img.shields.io/twitter/follow/radzima.svg?style=social "Follow @radzima"
[li]: https://linkedin.com/in/radzima "Ryan M. Adzima"
[twitter]: https://twitter.com/radzima "@radzima"
[website]: https://twoevilgeniuses.com "Two Evil Geniuses, LLC"
[paypal]: https://paypal.me/radzima "Donate"
[paypal-badge]: https://img.shields.io/badge/Donate-PayPal-blue.svg?style=flat-square "Donate"
[license_file]: /LICENSE "LICENSE"

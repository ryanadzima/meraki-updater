# meraki-updater
Update Meraki devices in a network using the provisioning API. Any information in the CSV will overwrite the dashboard values (including tags) so anything that should not be updated should be empty as shown in the example file. The CSV file should have the following columns: serial,name,tags,lat,lng,address.

Usage:

  Update devices in a single network from CSV:

        meraki-updater.py -k <MERAKI-PROVISIONING-API-KEY> -f <CSV-UPDATE-FILE>

  Update devices from a CSV with network specified per device:

        meraki-updater.py -k <MERAKI-PROVISIONING-API-KEY> -m -f <CSV-UPDATE-FILE>

  Write all devices on all accessible networks to a CSV (This file WILL be overwritten):

        meraki-updater.py -k <MERAKI-PROVISIONING-API-KEY> -g -o <CSV-OUTPUT-FILE>

  Arguments:

        -k/--key            Set the Meraki Provisioning API key (required)
        -f/--file           Set the CSV file to read for device updates
        -o/--output         Set the CSV file to write network devices (This file WILL be overwritten)
        -g/--get            Get network devices from all networks and write them to CSV
        -m/--multinetwork   Update devices across multiple networks using a CSV
        -v/--ver/--version  Display the version of this script


##### Author: [Ryan M. Adzima](https://linkedin.com/in/radzima)
##### Twitter: [@radzima](https://twitter.com/radzima)
##### Website: [Two Evil Geniuses](https://twoevilgeniuses.com)

License
=======

GNU General Public License v3.0

See `LICENSE <LICENSE>`_ to see the full text.

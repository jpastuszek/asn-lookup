This program will load ASN database from https://iptoasn.com/ and cache it for quick access later on.
Provided list of IPs to standard input (can be CSV format) or via command line parameters it will try to match ASN network address and provide it in format that is suited for inclusion in Puppet config file.

Example usage:
```sh
$ asn_lookup <<EOF
IP,Count
"104.144.128.205",743
"104.168.100.175",713
"23.254.46.82",712
"104.144.19.253",706
"138.128.84.128",693
EOF
'23.254.32.0/20', # CA 55286 SERVER-MANIA - B2 Net Solutions Inc. (23.254.46.82)
'104.144.16.0/21', # CA 55286 SERVER-MANIA - B2 Net Solutions Inc. (104.144.19.253)
'104.144.128.0/21', # CA 55286 SERVER-MANIA - B2 Net Solutions Inc. (104.144.128.205)
'104.168.100.0/23', # US 36352 AS-COLOCROSSING - ColoCrossing (104.168.100.175)
'138.128.84.0/22', # CA 55286 SERVER-MANIA - B2 Net Solutions Inc. (138.128.84.128)
```

# OpenRelayHunter

Not-So-Quick and dirty script to scan a selection of IP ranges for Open SMTP, DNS resolvers plus a few other useful utilities

Prerequisite: 'prips' utility (aptitude install prips)

Prerequisite: 'mail' utility (aptitude install mutt)

Authors: Johnathan Williamson (@SuitedUpGeek) / Shane Mc Cormack (@ShaneMcC)

Credits: Alain Kelder (http://goo.gl/TNQXSq
```
OpenRelay Hunter.

Usage: ./hunter.sh [flags] <IP> [IP [IP] ... [IP]]

Accepted flags:

 -h, --help                      Show this help.
 -d, --dns                       Check for Open DNS Resolver.
 -s, --smtp                      Check for Open Relay.
 -b, --heartbleed                Check for SSL Heartbleed Vulnerability." >&2
 -i, --superipmi                 Check for SuperMicro IPMI Vulnerability." >&2
 -B, --blacklist		 Check for RBL Listings." >&2
 -t <addr>, --to <addr>          Email address to send report to.
 -f <addr>, --from <addr>        Email address to send report from.

Anything param passed that isn't a flag is considered an address range to scan

!! Address ranges must be a CIDR range of /31 or larger, or individual IPs (without '/32') !!

OpenRelayHunter is licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License.
http://creativecommons.org/licenses/by-nc-sa/4.0/

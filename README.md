# gen-openpgp-rr - generate OpenPGP RR (to be used with DANE)
=============================================================

Usage
-----

`./gen-openpgp-rr <#keyid>`

This script creates DNS RR for every UID found for the given #keyid. #keyid
may be any key identifier (long or short ID or email address) as long as
`gpg --list-keys <#keyid>` finds exactly one key!

The RR lines could be directly added to the corresponding zone files and
should comply with https://tools.ietf.org/html/draft-ietf-dane-openpgpkey-01


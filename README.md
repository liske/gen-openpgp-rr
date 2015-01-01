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


Example
-------

```console
$ ./gen-openpgp-rr 49D0C2C3
; 49D0C2C3 - thomas@fiasko-nw.net
9f61c81cb2904274a2d20e8dc649dc5762cdefc93be4452d82ee4d16._openpgpkey.fiasko-nw.net.     IN      OPENPGPKEY mQGiBEEVL6YRBACSY2n1koQKEV2/UK0q8E+CFn/NIg9C9QCeVDnXILVaftfrR7x2uWTyvo0IhZ/LgIk2b+INiGRc4Rsx3vuDj6cvbAG9a2e+kS8ntfYwutwkOVgzUzV6X4Ok6Y02g0/6UlHWrvkE+DxWjXLCsxTqneNk0p9kXqUsmNdUVSM9JVm2QwCgoT1zWBJRJDJp4jzBR15flePvLukD/0O/lzmfsBcH0V851Hva2KMGJVI2XI2IWt++9l0hRHveaHs7YN5LJBHQhWSX+HH32fmXREf54aXrjFSzZYRstV5lO2wSVLZKV3AxJFKqmlXETJrtpwTHVpuglpE4xznu+kRGHg7mY+FJWzIDDzT+jDfzv3ViRRFAF23RvARbeIIPA/9yeV34PD2TrjPjrRuTL2hmXAPWoXysqb6kRrNSIc3drMgW6Ti5cBSjnIjMPEF/gQGdiJMDfpY6cjBlWP2R3wkZdpWLJEuHdJlXo/rvmplIi24tupalf9NHhUeTO/xDPj+GeKAGzFv1NG5ZAab6I6vROJBZZfWh4eQ00Iil2kLaQLQjVGhvbWFzIExpc2tlIDx0aG9tYXNAZmlhc2tvLW53Lm5ldD6IZQQTEQIAJQIbIwIeAQIXgAIZAQUCUU8/sQYLCQgHBAoFFQoJCAsFFgIDAQAACgkQjCsLJknQwsNVpACfQ0Mz3oUJw6rzFh9yUc2kprL+RfEAn0QA7WzcNzc5GGZPuEzhA7aaLppetCdUaG9tYXMgTGlza2UgPHRob21hc0BmaWFza28uZHluZG5zLm9yZz6IXwQTEQIAHwIeAQIXgAUCUU8/tAYLCQgHBAoFFQoJCAsFFgIDAQAACgkQjCsLJknQwsNn4wCbBUuxl4dLtdqdnJAFvbr/dz4thgsAn1oD4QxfjTRdr0oCp5O4pw8T3exbtCJUaG9tYXMgTGlza2UgPHRob21hcy5saXNrZUB3ZWIuZGU+iGEEExEIACEFAlREJJ0CGyMFCwkIBwMFFQoJCAsFFgIDAQACHgECF4AACgkQjCsLJknQwsNm+QCeN9OroW9xhoVFAdL4qOpz78xZUpAAnj3DHragBdTztn56MIDuHfisVQNAuQINBEEVL7EQCADPwth1mR/XA2OeU9gblkwBaecTrPRQ+8PwhELAldEaX8hhIq9Q/SNVEYwwLiaUzqfrRc4s6PS3V3f8cl09nL57ySCye3r4WUGvlp3FG8C/yayvxeApvpYSdPnxTEShzrB081SCQjeHzQ+HKBpMj04VbVrSpA4xboD081FdK18vqxLvitud6pJEXe2EyH9TN8pZinPydn3mALTawUt6LJh+Z8fwekqF/HE2erIbzwR4Lngbtnyoi2xav/NosUHOXeBVDZvct+fmA4oorrUX+a7CCEUCgZXcVjeyxQ/DsfFX5sRYQ/LGDsu8zDUluhEGNrd/r9t7l6Ndtac4ZMbUeJOPAAMFCAC+4vgCoX0Fa7ZCQdYSyv9bkBXj4Zd+QUZzXWfWlNRsYnEGAyjeSHyeRbQEQ4wPok1+LRoEzn+0UsFvP2Hk/95EdHLc84HTaSucQpav90FkR6R2MtrWLXUqMCTA+fD+HTJhBmJD7DvU0P0Swct9rhspw4WgtX6quJ8MsuEfIXgI5NeqAj51Toh8DRdzE5FM4FPGLHgJ8cpQZfTUNZxg2OH4kBNm3zCvTn7EY9jELyYjWQEKikO67q96IbEAEg9HYIa2ldn4XuaUoNX7XeTemie5/g6ew2NtKB+P3BesZnWiCqDdAQO+uwFGID1CmPCwTu51TZ6vcZaTHec3+EraxUiTiEYEGBECAAYFAkEVL7EACgkQjCsLJknQwsNRZQCfaa/DPDB2WEbjChy0llw2PsOxpPIAoI57hRpEQOhetD4Bn3gHHECR1sGC

```

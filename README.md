# RFC 8212 compliance tracking

[RFC 8212](https://tools.ietf.org/html/rfc8212) updates the core BGP
specification ([RFC 4271](https://tools.ietf.org/html/rfc4271)) by defining the
default behavior of a BGP speaker when there is no Import or Export Policy
associated with an External BGP session.

## Contributions

If you observe a mistake on this page or if you can contribute an update, please file a pull-request or email job@ntt.net. If you can include version numbers or point to public documentation that would be ideal.

# Compliant BGP implementations

* Cisco IOS XR
* BIRD (version 2.0.1 and higher)
* OpenBGPD (OpenBSD 6.4 and higher)
* Nokia SR OS (19.5.R1 or higher)
* FRRouting (7.4 or higher)
* Bio routing / bio-rd

# Non-compliant BGP implementations

* Arista EOS <sup>[1](#fn1)</sup>
* Cisco IOS (classic) / NX-OS
* Cisco IOS XE <sup>[2](#fn2)</sup>
* Juniper Junos <sup>[3](#fn3)</sup>
* Quagga
* Extreme IronWare

# Footnotes

<a name="fn1">1</a>: Arista EOS 4.18.0f allow you to emulate RFC 8212 behaviour by configuring the below, however this is not the default as of yet:
```
bgp missing-policy direction in action deny
bgp missing-policy direction out action deny
```
<br />
<a name="fn2">2</a>: IOS XE 17.2.1 allow you to emulate RFC 8212 behaviour by configuring the below, however this is not the default as of yet:
```
bgp safe-ebgp-policy
```
<br />
<a name="fn3">2</a>: Adam Chappell wrote a <a href="https://github.com/packetsource/rfc8212-junos">RFC 8212 SLAX script</a> to side-load a RFC 8212 shim on Junos devices.<br />

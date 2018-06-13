# RFC 8212 compliance tracking

[RFC 8212](https://tools.ietf.org/html/rfc8212) updates the core BGP
specification ([RFC 4271](https://tools.ietf.org/html/rfc4271)) by defining the
default behavior of a BGP speaker when there is no Import or Export Policy
associated with an External BGP session.

## Contributions

If you observe a mistake on this page or if you can contribute an update, please file a pull-request or email job@ntt.net. If you can include version numbers or point to public documentation that would be ideal.

# Compliant BGP implementations

* Cisco IOS XR (all versions)
* BIRD (version 2.0.1 and higher)
* OpenBGPD (OpenBSD 6.4 and higher)

# Non-compliant BGP implementations

* Arista EOS <sup>[4](#fn1)</sup>
* Cisco IOS (classic)
* Cisco IOS-XE
* Cisco NX-OS
* Juniper Junos
* Nokia SR OS <sup>[2](#fn2)</sup>
* Quagga
* frr

# Footnotes

<a name="fn2">2</a>: Greg Hankins from Nokia indicated that Nokia is <a href="https://mailarchive.ietf.org/arch/msg/idr/kgl6etbjUuR3jLHVeDSi4LLIs50">working on compliance</a>.<br />
<br />
<a name="fn4">4</a>: Arista EOS 4.18.0f allow you to emulate RFC 8212 behaviour by configuring the below, however this is not the default as of yet:
```
bgp missing-policy direction in action deny
bgp missing-policy direction out action deny
```
<br />

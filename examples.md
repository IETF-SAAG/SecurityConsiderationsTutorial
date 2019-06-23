# Examples

### draft-ietf-idr-te-pm-bgp-13

This is an example of security considerations by reference

```
   Procedures and protocol extensions defined in this document do not
   affect the BGP security model.  See the 'Security Considerations'
   section of [RFC4271] for a discussion of BGP security.  Also refer to
   [RFC4272] and [RFC6952] for analysis of security issues for BGP.
```
* RFC 4271 is BGP. The model may be the same, but this is new information being sent out.
```
   The TLVs introduced in this document are used to propagate IGP
   defined information ([RFC7810] and [RFC7471].)  These TLVs represent
   the state and resources availability of the IGP link.  The IGP
   instances originating these TLVs are assumed to have all the required
   security and authentication mechanism (as described in [RFC7810] and
   [RFC7471]) in order to prevent any security issue when propagating
   the TLVs into BGP-LS.
```
* RFC 7810 and 7471 describe sending TE information in IS-IS and OSPF respectively. 
* But IS-IS and OSPF run in different environments than BGP.
  * IS-IS and OSPF run in a local network, while BGP is the Internet
* It is not clear that information that is fine to send in OSPF is fine to send in BGP
  * The Security Considerations section should specifically say this. 

:sheep:

### draft-ietf-lamps-pkix-shake-08

This is an example of irrelevant information

```
   The SHAKEs are deterministic functions.  Like any other deterministic
   function, executing multiple times with the same input will produce
   the same output.  Therefore, users should not expect unrelated
   outputs (with the same or different output lengths) from running a
   SHAKE function with the same input multiple times.  The shorter of
   any two outputs produced from a SHAKE with the same input is a prefix
   of the longer one.  It is a similar situation as truncating a 512-bit
   output of SHA-512 by taking its 256 left-most bits.  These 256 left-
   most bits are a prefix of the 512-bit output.
```
* All true, but not really related to using the SHAKE functions in PKIX.

```
   When using ECDSA with SHAKEs, the ECDSA curve order SHOULD be chosen
   in line with the SHAKE output length.  NIST has defined appropriate
   use of the hash functions in terms of the algorithm strengths and
   expected time frames for secure use in Special Publications (SPs)
   [SP800-78-4] and [SP800-107].  These documents can be used as guides
   to choose appropriate key sizes for various security scenarios.  In
   the context of this document id-ecdsa-with-shake128 is RECOMMENDED
   for curves with group order of 256-bits. id-ecdsa-with-shake256 is
   RECOMMENDED for curves with group order of 384-bits or more.
```
* This is actually quite good. It instructs the user or (more likely) future document authors about where to use the SHAKE functions and with what curves they should be combined. 
* This is not necessary for a fully compliant implementation, but it helps with where this function is to be used.

:sheep:

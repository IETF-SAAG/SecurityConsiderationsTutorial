# What does not go into the security considerations section

but sometimes we see people put it there anyway...

## Normative text
* By this, we mean mechanisms and things needed, usually winds up here because of trying to fix something.
* Not a hard-and-fast rule
* The MUSTs and SHOULDs for your protocol go elsewhere
** Even if they're for using a security mechanism

Ideal security considerations text has a lot of "As explained in section X", or "the foobar attack is
mitigated by the actions of section Y, step 4"...

### Examples:
* Wrong:
  * The uniqString value mentioned in section 4 MUST be 256 high quality random bits.
  * The RSA key in section 4.1 MUST be at least 3072 bits in length and MUST be chosen using one of the approved methods described in [SP800-56B]
* Right:
  * Section 4 requires uniqString to be 256 high quality random bits to avoid birthday attacks.
  * The key length and generation requirements in section 4.1 represent the current state of the art assuming an attacker not equipped with a large-scale quantum computer.

:sheep:

*Need more...*

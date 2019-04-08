# What goes into a Security Considerations Section

This part of the tutorial tells what things should be covered in the section. Some of it is based on RFC 3552, some may be based on the -00 [draft](https://tools.ietf.org/html/draft-nir-saag-rfc3552bis-00) that tried to revise 3552; and some may be new.

## The Internet Threat Model
(5 slides to introduce terminology. Not sure the below subjects are the best)
### Threat models
### Active/Passive Attacks
### Mass Surveillance
### On-path vs Off-path
### Authentication and Authorization

:sheep:

## What MUST go in the Security Considerations Section
(each of the following sub-sections may be 1-3 slides)
### In- and Out- of scope threats and attacks.
### Security of the Authentication
### Threat environment
* Usually this is the Internet Threat Model
  * Doesn't need to be stated if that's it
* Usually includes deployment across the global Internet
* If your protocol is special, call out the threat environment

Example:
* PTPv2 requires that jitter be kept at sub-micro- or sub-nano-second levels.
* It cannot have a router between the endpoints because routers do queueing.
* Its threat environment is very different to that of anything that runs over the Internet.

### Residual Risk
### Risks resulting from foreseen misapplication or mis-deployment
### Call out information that is sent out
(Especially user information)

:sheep:




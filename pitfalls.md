# Pitfalls

This section lists common pitfalls SecDir reviewers have seen in Security Considerations sections.

## Security Considerations by Reference
* "This does not change the security properties of the base protocol"
  * But this extension sends information that was never sent before
    * Used to be the IP address of a server; now it's the name and phone number of the admin.
* Don't go more than one level deep in indirection
* Call out what's changed.

## Security Considerations by Similarity
* "This is just the same as that other RFC for that other protocol"
  * But it's not all the same, is it?
    * One piece of information is not like another (IP address vs admin name)
    * One protocol is not like another (BGP vs OSPF)
    * One network is not the same as another (corporate network vs data center vs cloud vs the Internet)

## Just use IPsec / TLS / TLS with ACME / I2NSF
* Each of these takes a serious effort to deploy
* Is there a good plan for the people deploying your protocol to deploy these as well?


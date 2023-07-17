# quic-in-space-hackathon
Hackathon to get QUIC working in Space scenarios: aka long delays and disruptions.

## Rationale
- QUIC is a new transport bringing very interesting features that could enable its use in space, while TCP is not good. However, QUIC was designed for terrestrial Internet, which brings assumptions on typical delays and connectivity. In (deep) space, delays are much larger, in order of minutes (4-20 minutes to Mars), and long disruptions, such as because of orbital mechanics, in order minutes or hours or days. 
- It may be possible to modify the base behavior of QUIC stacks to satisfy these requirements. For example, several assumptions, such as initial delay, are just static constants in the code that could be externalized so they could better start the QUIC machinery in the context of space.
- Purpose of this project is to modify open-source QUIC stacks to work in this use case. 
- The following tasks are envisionned:
  - externalize these static values so they could be changed at start or while running
  - set a testbed to test with long delays and verify use
  - modify stacks to support the space use case (specially for disruptions)
  - if relevant, write internet-draft for findings and possible modifications/extensions to QUIC
- An initial POC was done with Christian Huitema (see below) with his picoquic stack. 
  We would like to go further with more QUIC stacks such as Mozilla Neqo (in Rust) or 
  Google Quiche(in C++) or Cloudflare Quiche (in Rust) or picoquic(in C) or QUINN (in Rust).

## IETF 117 SFO Hackathon Information
- [Hackathon main web page](https://wiki.ietf.org/en/meeting/117/hackathon)
- Saturday - Sunday, 22-23 July 2023; Hilton Union Square, San Francisco, CA, USA; Plaza A-B, Lobby Level
- [IETF Zulip hackathon channel](https://zulip.ietf.org/#streams/326/hackathon) will be used for instant messaging
- **Champion(s)**
  - Marc Blanchet (marc.blanchet at viagenie.ca)
  - Christian Huitema (huitema at huitema.net)
- **Additional Info**
  - [POC](https://www.privateoctopus.com/2023/02/07/quic-to-mars.html)
  - [Mozilla Neqo](https://github.com/mozilla/neqo)
     - [Example to externalize an internal parameter](https://github.com/mozilla/neqo/pull/1402)
  - [Cloudflare Quiche](https://github.com/cloudflare/quiche)
  - [Google Quiche](https://github.com/google/quiche)
  - [Huitema Picoquic](https://github.com/private-octopus/picoquic)
  - [Quinn](https://github.com/quinn-rs/quinn)
  - [Linux Netem (to introduce delay)](https://man7.org/linux/man-pages/man8/tc-netem.8.html)
  - [MacOSX Network Link Conditioner (to introduce delay)](https://medium.com/@itsanurag/simulate-low-network-with-network-link-conditioner-a1a7f14423b6)

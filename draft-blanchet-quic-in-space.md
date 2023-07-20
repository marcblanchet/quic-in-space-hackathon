---
###
# Internet-Draft Markdown Template
#
# Rename this file from draft-todo-yourname-protocol.md to get started.
# Draft name format is "draft-<yourname>-<workgroup>-<name>.md".
#
# For initial setup, you only need to edit the first block of fields.
# Only "title" needs to be changed; delete "abbrev" if your title is short.
# Any other content can be edited, but be careful not to introduce errors.
# Some fields will be set automatically during setup if they are unchanged.
#
# Don't include "-00" or "-latest" in the filename.
# Labels in the form draft-<yourname>-<workgroup>-<name>-latest are used by
# the tools to refer to the current version; see "docname" for example.
#
# This template uses kramdown-rfc: https://github.com/cabo/kramdown-rfc
# You can replace the entire file if you prefer a different format.
# Change the file extension to match the format (.xml for XML, etc...)
#
###
title: "QUIC in Space"
abbrev: "QUIC in Space"
category: info

docname: draft-blanchet-quic-in-space-latest
ipr: "trust200902"
submissiontype: IETF
number:
date:
consensus: true
v: 3
area: transport
workgroup: Quic
keyword:
 - quic
 - delay tolerant
 - space communication
venue:
  group: WG
  type: Working Group
  mail: quic@ietf.com
  github: blanchet/quic-in-space-hackathon
  latest: https://example.com/LATEST

author:
 -
    fullname: Marc Blanchet
    organization: Viagenie
    email: marc.blanchet@viagenie.ca
 -
    fullname: Christian Huitema
    organization: Private Octopus Inc.
    email: huitema@huitema.net

normative:

informative:


--- abstract

Discuss the challenges of running QUIC in space.
Incorporate results from Hackathon at IETF 117.
Provide guidance to implementations.

--- middle

# Introduction

QUIC is a new transport bringing very interesting features that could enable its use in space, while TCP is not good. However, QUIC was designed for terrestrial Internet, which brings assumptions on typical delays and connectivity. In (deep) space, delays are much larger, in order of minutes (4-20 minutes to Mars), and long disruptions, such as because of orbital mechanics, in order minutes or hours or days.

It may be possible to modify the base behavior of QUIC stacks to satisfy these requirements. For example, several assumptions, such as initial delay, are just static constants in the code that could be externalized so they could better start the QUIC machinery in the context of space.

The purpose of this document is to provide guidance for supporting space communication in QUIC implementations.


# Conventions and Definitions

{::boilerplate bcp14-tagged}

# Implementation Guidance

TODO: pay attention to delays.


# Security Considerations

TODO Security


# IANA Considerations

This document has no IANA actions.


--- back

# Acknowledgments
{:numbered="false"}

TODO acknowledge.

---
title: "Normalized Representation of YANG State Data"
abbrev: "yang-state-normalization"
category: std

docname: draft-mendez-opsawg-yang-state-normalization-latest
submissiontype: IETF  # also: "independent", "editorial", "IAB", or "IRTF"
number:
date:
consensus: true
v: 3
area: "Operations and Management"
workgroup: "Operations and Management Area Working Group"
keyword:
 - normalization
 - datastore
 - semantic representation
venue:
  group: "Operations and Management Area Working Group"
  type: "Working Group"
  mail: "opsawg@ietf.org"
  arch: "https://mailarchive.ietf.org/arch/browse/opsawg/"
  github: "ana-mp26/yang-state-normalization"
  latest: "https://ana-mp26.github.io/yang-state-normalization/draft-mendez-opsawg-yang-state-normalization.html"

author:
 -  fullname: Ana Méndez
    organization: Telefonica
    email: "ana.mendezperez@telefonica.com"
 -  fullname: Diego López
    organization: Telefonica
    email: "diego.r.lopez@telefonica.com"
 -  fullname: Jan Lindblad
    organization: All For Eco
    email: "jan.lindblad+ietf@for.eco"

normative:

informative:

...

--- abstract

This document defines a normalization procedure for YANG state data. The procedure enables semantically equivalent YANG data to produce equivalent normalized representations independently of the serialization format and applicable representation conventions.
 
The normalized representation is intended to support comparison, hashing, integrity verification, provenance, and other procedures
that require stable identification of equivalent YANG state data.


--- middle

# Introduction {#intro}

TODO Introduction


# Conventions and Definitions

{::boilerplate bcp14-tagged}


# Security Considerations {#security}

TODO Security


# IANA Considerations {#iana}

This document has no IANA actions.


--- back

# Acknowledgments
{:numbered="false"}

TODO acknowledge.

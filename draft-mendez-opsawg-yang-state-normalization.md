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
 
The normalized representation is intended to support comparison, hashing, integrity verification, provenance, and other procedures that require stable identification of equivalent YANG state data.

This version defines a schema-independent normalization profile and assumes that sibling ordering is not semantically significant.


--- middle

# Introduction {#intro}

# Introduction

YANG is widely used to model configuration data, operational state, notifications, and other information exchanged between network management systems.

Data modeled using YANG can be represented through different serialization formats, including XML, JSON, and CBOR. Furthermore, equivalent YANG-modeled information may be serialized differently by distinct implementations due to representation-specific conventions, ordering choices, or encoding mechanisms.

These differences make it difficult to determine whether two representations convey the same information. As a result, operations such as datastore comparison, data deduplication,fingerprint generation, integrity verification, provenance processing, and message-broker compaction often depend on representation-specific artifacts rather than on the underlying information itself.

Existing normalization and canonicalization mechanisms operate at the serialization level. For example, XML, JSON, and CBOR provide independent procedures for producing deterministic encodings of individual documents. However, these mechanisms do not address the broader problem of obtaining a common representation across different serialization formats.

This document defines a normalization procedure for YANG state data that produces a deterministic representation independent of the original serialization format. The procedure enables equivalent YANG-modeled information to converge into the same normalized representation, providing a stable basis for comparison, fingerprint generation, integrity verification, and other operational uses.

This version defines a schema-independent normalization profile. The procedure does not require access to the corresponding YANG schema and assumes that sibling ordering is not semantically significant.

## Scope

This document focuses on representation equivalence of YANG-modeled data.

The procedure defined in this document is intended to identify when different serialized representations convey equivalent information.

This document does not define a complete semantic normalization of YANG datastore contents. Schema-specific concepts such as default values, identityref resolution, leafref resolution, and ordered-by-user semantics are outside the scope of this version and may be addressed by future work or versions.


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

#Parent Address

**Version**: 1

**Purpose**: Verify that the association role “parentAddress” is populated for all addresses which are connected to a parent (or main) address.

**Prerequisites**

**Test method**

* Check that the [association role parentAddress](#parentAddress) is populated for all addresses which are connected to a parent (or main) address.
  
**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-ad/3.2/ad-as/README#ref_TG_DS_tmpl) IR requirement Section 5.5.2 (2)

**Test type**: Manual

**Notes**

## Messages

n/a

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-ad/3.1/ad-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
parentAddress association role <a name="parentAddress"></a>   | //schema-element(ad:Address)/ad:parentAddress

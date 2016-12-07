# Feature references

**Version**: 1

**Purpose**: Verify that referenced features can be retrieved.

**Prerequisites**

**Test method**

* Verify that any feature reference in an association role is publicly accessible via HTTP, i.e. inspect all relevant properties. If a reference (@xlink:href) has a value that starts with "#", verify that an element with a `gml:id` attribute with the referenced identifier exists in the same document. If the reference starts with "http", verify that a HTTP GET request to the URI retrieves an XML document. Otherwise report [brokenLink](#brokenLink).

This data theme currently has the following association roles:

* MarkerPost.[route](#route) : TransportPoint
* TransportLinkSet.[post](#post) : MarkerPost
* TrafficSeparationScheme.[component](#component) : TrafficSeparationSchemeArea
* TrafficSeperationScheme.[markerBuoy](#markerBuoy) : Buoy
* TrafficSeperationScheme.[marineWaterRoute](#marineWaterRoute) : MarineWaterway
* TrafficSeperationScheme.[markerBeacon](#markerBeacon) : Beacon

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ia/README#ref_TG_DS_tmpl) IR requirement Article 4 (2)

**Test type**: automated

**Notes**

* TrafficSeparationScheme is an abstract class. It does not have any subtypes.

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP. Every code list value must be made available in an online registry. 

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ia/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
route <a name ="route"></a>	| //schema-element(tn:MarkerPost)/tn:route/@xlink:href
post <a name ="post"></a>	| //schema-element(tn-ro:Road)/ad:post/@xlink:href or //schema-element(tn-ro:ERoad)/ad:post/@xlink:href
component <a name ="component"></a>	| 
markerBuoy <a name ="markerBuoy"></a>	| 
marineWaterRoute <a name ="marineWaterRoute"></a>	| 
markerBeacon <a name ="markerBeacon"></a>	| 
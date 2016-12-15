# network-connectivity

**Version**: 1

**Purpose**: Verify the connectivity of the transport network.

**Prerequisites**

n/a

**Test method**

Automated assertions:

* Verify that all transport nodes are at the start or end of a transport link. For each [TransportLink](#TransportLink) with a startNode or endNode property, verify that the distance between the start or end of the [centerlineGeometry](#geometry) and the geometry of the [start](#start) and [end](#end) [TransportNode](#TransportNodes) is smaller than the [connectivityTolerance](#tolerance). Otherwise report [noConnectionStart](#noConnectionStart) or [noConnectionEnd](#noConnectionEnd).
* For each [TransportLink](#TransportLink) verify that the only [TransportNodes](#TransportNodes) in the distance around the start or end of the [centerlineGeometry](#geometry) are the nodes associated via the [startNode](#start) and [endNode](#end) properties. Otherwise report [additionalNode](#additionalNode).

Manual assertions:

* Verify that the connectivity tolerance provided for the test is consistent with the metadata of the data set, i.e. check that the connectivity tolerance provided for the test is the same included in the metadata of the data set in the properties 'specification' and 'explanation' of the DQ\_ConformanceResult element in a DQ\_TopologicalConsistency element.

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_tmpl) IR requirement Section 8.7.7 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_tmpl) IR requirement Section 8.7.7 (2)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_tmpl) IR requirement Section 8.7.7 (3)

**Test type**: Automated/Manual

**Notes**

Geometries typically will need to be converted into a meter-based CRS, eg ETRS89 LAEA or LCC. 

It is unclear how to handle geometries outside of continental Europe. Classify all assertions as "manual"?

No test is included for the following requirement, which is unclear: "In data sets where both transport links and nodes are present, the relative position of nodes and link ends in relation to the specified connectivity tolerance shall correspond to the associations that exist between them in the data set." What should be tested?

## Parameters

Identifier  |  Description
---------------------------------------------------------- | -------------------------------------------------------------------------
connectivityTolerance <a name="tolerance"/>  |  a number, the tolerance in meter

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
noConnectionStart <a name="noConnectionStart"/>  |  XML document '$filename', TransportLink '$gmlid': The TransportNode '$gmlidNode' at the start of the link (coordinates: '$coordNode') is spatially not located at the start of the link (coordinates: '$coordStart').
noConnectionEnd <a name="noConnectionEnd"/>  |  XML document '$filename', TransportLink '$gmlid': The TransportNodeNode '$gmlidNode' at the end of the link (coordinates: '$coordNode') is spatially not located at the end of the link (coordinates: '$coordStart').
additionalNode <a name="additionalNode"/>  |  XML document '$filename', TransportLink '$gmlid': TransportNodeNode '$gmlidNode' is located within the connectivity tolerance of the start or end of the link geometry, but is not a start or end node of the link.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
TransportLink <a name="TransportLink"></a>   | //schema-element(hy-n:TransportLink)[net:startNode or net:endNode] 
centerlineGeometry <a name="geometry"></a>   | $TransportLink/net:centerlineGeometry 
start <a name="start"></a>   | $TransportLink/net:startNode/hy-n:TransportNodeNode/net:geometry 
end <a name="end"></a>   | $TransportLink/net:endNode/hy-n:TransportNodeNode/net:geometry 
TransportNodeNodes <a name="TransportNodes"></a>   | //schema-element(hy-n:TransportNodeNode) 
startNode <a name="start"></a>   | $TransportLink/net:startNode 
endNode <a name="end"></a>   | $TransportLink/net:endNode 


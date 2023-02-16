# Geometry

**Version**: 1

**Purpose**: Verify geometric consistency, i.e. check that geometries are consistent with the geometries of other features in the data set.

**Prerequisites**

**Test method**

Automated assertions:

* If the TransportNode and the TransportLink feature types are contained in the same dataset, using a geometry library, verify for each [TransportNode](#TransportNode) that the [geometry](#geometry) (a gml:Point) is located a position that touches a [TransportLink](#TransportLink).[centerlineGeometry](#centerlineGeometry) (a gml:LineString or gml:Curve), i.e. that the node is at the start or end of a transport link. If the check fails report [freeNode](#freeNode).

  *  Otherwise, if the TransportNode and the TransportLink feature types are not contained in the same dataset, a manual check is required to verify that for each [TransportNode](#TransportNode) the [geometry](#geometry) (a gml:Point) is located a position that touches a [TransportLink](#TransportLink).[centerlineGeometry](#centerlineGeometry) (a gml:LineString or gml:Curve), in this case report the message [freeNodeManualCheck](#freeNodeManualCheck).

Manual assertions:

* Verify that transport link connections are consistent with the real world, i.e. check that TransportLink features ends are connected wherever a connection exists between the real world phenomena they represent. No connections must be created at connecting network elements when it is not possible for water to pass from one element to another.

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-as/README#ref_TG_DS_tmpl) IR requirement Section 7.9.3 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-as/README#ref_TG_DS_tmpl) IR requirement Section 7.9.3 (2)

**Test type**: Automated/Manual

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
freeNode <a name="freeNode"/>  |  XML document '$filename', TransportNode '$gmlid': The node is not located at the start or end of any TransportLink feature in the data set.
freeNodeManualCheck <a name="freeNodeManualCheck"/>  |  XML document '$filename', TransportNode '$gmlid': The relevant TransportLink feature is not available in the data set, manually verify that the TransportNode geometry (a gml:Point) is located at a position that touches a TransportLink.centrelineGeometry (a gml:LineString or gml:Curve), i.e. that the node is at the start or end of a transport link.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
TransportNode <a name="TransportNode"></a> 	| 	//schema-element(tn-ro:RoadNode) or //schema-element(tn-ra:RailwayNode) or //schema-element(tn-ra:RailwayYardNode) or //schema-element(tn-ra:RailwayStationNode) or //schema-element(tn-c:CablewayNode) or //schema-element(tn-w:WaterwayNode) or //schema-element(tn-w:PortNode) or //schema-element(tn-a:Navaid) or //schema-element(tn-a:DesignatedPoint) or //schema-element(tn-a:RunwayCentrelinePoint) or //schema-element(tn-a:TouchDownLiftOff) or //schema-element(tn-a:AerodromeNode)
geometry <a name="geometry"></a>   | $TransportNode/*/gml:Point
TransportLink <a name="TransportLink"></a> 	| 	//schema-element(tn-ro:RoadLink) or //schema-element(tn-ra:RailwayLink) or //schema-element(tn-c:CablewayLink) or //schema-element(tn-w:WaterwayLink) or //schema-element(tn-a:AirRouteLink) or //schema-element(tn-a: ProcedureLink) or //schema-element(tn-a:StandardInstrumentDeparture) or //schema-element(tn-a:InstrumentApproachProcedure) or //schema-element(tn-a:StandardInstrumentArrival)
TransportLink.centerlineGeometry <a name="centerlineGeometry"></a>   | $TransportLink/tn:centerlineGeometry 

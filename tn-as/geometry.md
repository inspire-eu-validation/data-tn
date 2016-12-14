# Geometry

**Version**: 1

**Purpose**: Verify geometric consistency, i.e. check that geometries are consistent with the geometries of other features in the data set.

**Prerequisites**

**Test method**

Automated assertions:

* Using a geometry library, verify for each [TransportNode](#TransportNode) that the [geometry](#geometry) (a gml:Point) is located a position that touches a [TransportLink](#TransportLink).[centerlineGeometry](#centerlineGeometry) (a gml:LineString or gml:Curve), i.e. that the node is at the start or end of a transport link. Otherwise report [freeNode](#freeNode).

Manual assertions:

* Verify that transport link connections are consistent with the real world, i.e. check that TransportLink features ends are connected wherever a connection exists between the real world phenomena they represent. No connections must be created at connecting network elements when it is not possible for water to pass from one element to another.

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.1/tn-as/README#ref_TG_DS_tmpl) IR requirement Section 7.9.3 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.1/tn-as/README#ref_TG_DS_tmpl) IR requirement Section 7.9.3 (2)

**Test type**: Automated/Manual

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
freeNode <a name="freeNode"/>  |  XML document '$filename', HydroNode '$gmlid': The node is not located at the start or end of any TransportLink feature in the data set.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-tn/3.1/tn-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
TransportNode <a name="TransportNode"></a> 	| 	//schema-element(tn-ro:RoadNode) or //schema-element(tn-ra:RailwayNode) or //schema-element(tn-ra:RailwayYardNode) or //schema-element(tn-ra:RailwayStationNode) or //schema-element(tn-ca:CablewayNode) or //schema-element(tn-w:WaterwayNode) or //schema-element(tn-w:PortNode) or //schema-element(tn-a:Navaid) or //schema-element(tn-a:DesignatedPoint) or //schema-element(tn-a:RunwayCentrelinePoint) or //schema-element(tn-a:TouchDownLiftOff) or //schema-element(tn-a:AerodromeNode)
geometry <a name="geometry"></a>   | $TransportNode/*/gml:Point
TransportLink <a name="TransportLink"></a> 	| 	//schema-element(tn-ro:RoadLink) or //schema-element(tn-ra:RailwayLink) or //schema-element(tn-ca:CablewayLink) or //schema-element(tn-w:WaterwayLink) or //schema-element(tn-a:AirRouteLink) or //schema-element(tn-a: ProcedureLink) or //schema-element(tn-a:StandardInstrumentDeparture) or //schema-element(tn-a:InstrumentApproachProcedure) or //schema-element(tn-a:StandardInstrumentArrival)
TransportLink.centerlineGeometry <a name="centerlineGeometry"></a>   | $TransportLink/tn:centerlineGeometry 
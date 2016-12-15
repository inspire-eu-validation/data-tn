# Spatial consistency

**Version**: 1

**Purpose**: Verify that the spatial information is consistent.

**Prerequisites**

n/a

**Test method**

Verify that transportation networks are spatially connected across data sets.

Automated assertions:

* Use a geometry library to verify for each [TransportLink](#TransportLink) that its [centrelineGeometry](#centrelineGeometry) is within the [geometry](#geometry) of a single [TransportArea](#TransportArea). Verify for each [TansportNode](#TransportNodeNode) that its geometry is within a [TransportArea](#TransportArea) feature, too. Otherwise report [notWithin](#notWithin).


Manual assertions:

* Review the data maintenance procedures and perform spot checks to verify that connectivity between transportation networks across state borders and – where applicable – also across regional borders (and data sets) within Member States is established and maintained by the respective authorities, using the cross-border connectivity mechanisms provided by the NetworkConnection type.

**Reference(s)**: 

* [TG DS-TN](http://inspire.ec.europa.eu/id/ats/data-tn/3.1/tn-dc/README#ref_TG_DS_TN) IR requirement Section 7.9.1 (1)
* [TG DS-TN](http://inspire.ec.europa.eu/id/ats/data-tn/3.1/tn-dc/README#ref_TG_DS_TN) IR requirement Section 7.9.1 (2)

**Test type**: Automated/Manual

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
notWithin <a name="notWithin"/>  |  XML document '$filename', $featureType '$gmlid': The geometry is not within a single SurfaceWater feature from the Physical Waters application schema.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-tn/3.1/tn-dc/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
TransportLink <a name="TransportLink"></a>   | //schema-element(tn-ro:RoadLink) or //schema-element(tn-ra:RailwayLink) or //schema-element(tn-ca:CablewayLink) or //schema-element(tn-w:WaterwayLink) or //schema-element(tn-a:AirRouteLink) or //schema-element(tn-a: ProcedureLink) or //schema-element(tn-a:StandardInstrumentDeparture) or //schema-element(tn-a:InstrumentApproachProcedure) or //schema-element(tn-a:StandardInstrumentArrival)
TransportArea <a name="TransportArea"></a>   | //schema-element(tn-ro:RoadServiceArea) or //schema-element(tn-ro:RoadArea) or //schema-element(tn-ro:VehicleTrafficArea) or //schema-element(tn-ra:RailwayArea) or //schema-element(tn-ra:RailwayStationArea) or //schema-element(tn-ra:RailwayYardArea) or //schema-element(tn-w:FairwayArea) or //schema-element(tn-w:PortArea) or //schema-element(tn-w:TrafficSeparationSchemeCrossing) or //schema-element(tn-w:TrafficSeparationSchemeLane) or //schema-element(tn-w:TrafficSeparationSchemeRoundabout) or //schema-element(tn-w:TrafficSeparationSchemeSeperator) or //schema-element(tn-a:AerodromeArea) or //schema-element(tn-a:AirspaceArea) or //schema-element(tn-a:ApronArea) or //schema-element(tn-a:RunwayArea) or //schema-element(tn-a:TaxiwayArea)
TransportNode <a name="TransportNode"></a>   | //schema-element(tn-ro:RoadNode) or //schema-element(tn-ra:RailwayNode) or //schema-element(tn-ra:RailwayYardNode) or //schema-element(tn-ra:RailwayStationNode) or //schema-element(tn-ca:CablewayNode) or //schema-element(tn-w:WaterwayNode) or //schema-element(tn-w:PortNode) or //schema-element(tn-a:Navaid) or //schema-element(tn-a:DesignatedPoint) or //schema-element(tn-a:RunwayCentrelinePoint) or //schema-element(tn-a:TouchDownLiftOff) or //schema-element(tn-a:AerodromeNode)
centerlineGeometry <a name="centrelineGeometry"></a>   | $TransportLink/\*:centrelineGeometry
geometry <a name="geometry"></a>   | $TransportArea/\*:geometry
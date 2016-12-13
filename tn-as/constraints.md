# Constraints

**Version**: 1

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

Verify that the OCL constraints listed below that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation). 

For constraints that require retrieving a referenced resource and the resource cannot be retrieved, report [brokenLink](#brokenLink). The test accepts the following two types of content in @xlink:href attributes: Either a "#" followed by a @gml:id in the same document or a HTTP URI.

Automated tests:

* TrafficFlowDirection can only be associated with a spatial object of the type Link or LinkSequence; OCL: "inv: networkRef.element.oclIsKindOf(LinkReference)". Verify that an [TrafficFlowDirection](#TrafficFlowDirection) only has a [Network element association](#NetworkElement) with a spatial object [TransportLink](#TransportLink) or [TransportLinkSequence](#TransportLinkSequence).
* All transport areas have an external object identifier; OCL: "inv:inspireId->notEmpty()". Verify that all [TransportArea](#TransportArea) have an [inspireID](#inspireID).
* All transport links have an external object identifier; OCL: "inv:inspireId->notEmpty()". Verify that all [TransportLink](#TransportLink) have an [inspireID](#inspireID).
* All transport link sequences have an external object identifier; OCL: "inv:inspireId->notEmpty()". Verify that all [TransportLinkSequence](#TransportLinkSequence) have an [inspireID](#inspireID).
* All transport link sets have an external object identifier; OCL: "inv:inspireId->notEmpty()". Verify that all [TransportLinkSet](#TransportLinkSet) have an [inspireID](#inspireID).
* All transport nodes have an external object identifier; OCL: "inv:inspireId->notEmpty()". Verify that all [TransportNode](#TransportNode) have an [inspireID](#inspireID).
* All transport points have an external object identifier; OCL: "inv:inspireId->notEmpty()". Verify that all [TransportPoint](#TransportPoint) have an [inspireID](#inspireID).
* All transport properties have an external object identifier; OCL: "inv:inspireId->notEmpty()". Verify that all [TransportProperty](#TransportProperty) have an [inspireID](#inspireID).
* A transport link sequence must be composed of transport links that all belong to the same transport network; OCL: "inv: link->forAll(l | l.link.inNetwork = self.inNetwork)". Verify that all [TransportLinkSequence](#TransportLinkSequence) are composed of all [link](#link) that have the same value for the [inNetwork](#inNetwork) association role as the [TransportLinkSequence](#TransportLinkSequence).
* A transport link set must be composed of transport links and or transport link sequences that all belong to the same transport network; OCL: "inv: link->forAll(l | l.inNetwork = self.inNetwork)". Verify that all [TransportLinkSet](#TransportLinkSet) are composed of all [link](#link) that have the same value for the [inNetwork](#inNetwork) association role as the [TransportLinkSet](#TransportLinkSet).

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-TN](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-as/README#ref_TG_DS_TN)) 5.4

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
TrafficFlowDirection <a name="TrafficFlowDirection"></a> 	| 	//schema-element(tn:TrafficFlowDirection) or //schema-element(tn-w:WaterTrafficFlowDirection)
Network element association TrafficFlowDirection <a name="NetworkElement"></a> 	| 	//schema-element(tn:TrafficFlowDirection)/net:networkRef/*/net:element/@xlink:href or //schema-element(tn-w:WaterTrafficFlowDirection)/net:networkRef/*/net:element/@xlink:href
TransportArea <a name="TransportArea"></a> 	| 	//schema-element(tn-ro:RoadServiceArea) or //schema-element(tn-ro:RoadArea) or //schema-element(tn-ro:VehicleTrafficArea) or //schema-element(tn-ra:RailwayArea) or //schema-element(tn-ra:RailwayStationArea) or //schema-element(tn-ra:RailwayYardArea) or //schema-element(tn-w:FairwayArea) or //schema-element(tn-w:PortArea) or //schema-element(tn-w:TrafficSeparationSchemeCrossing) or //schema-element(tn-w:TrafficSeparationSchemeLane) or //schema-element(tn-w:TrafficSeparationSchemeRoundabout) or //schema-element(tn-w:TrafficSeparationSchemeSeperator) or //schema-element(tn-a:AerodromeArea) or //schema-element(tn-a:AirspaceArea) or //schema-element(tn-a:ApronArea) or //schema-element(tn-a:RunwayArea) or //schema-element(tn-a:TaxiwayArea)
TransportLink <a name="TransportLink"></a> 	| 	//schema-element(tn-ro:RoadLink) or //schema-element(tn-ra:RailwayLink) or //schema-element(tn-ca:CablewayLink) or //schema-element(tn-w:WaterwayLink) or //schema-element(tn-a:AirRouteLink) or //schema-element(tn-a: ProcedureLink) or //schema-element(tn-a:StandardInstrumentDeparture) or //schema-element(tn-a:InstrumentApproachProcedure) or //schema-element(tn-a:StandardInstrumentArrival)
TransportLinkSequence <a name="TransportLinkSequence"></a> 	| 	//schema-element(tn-ro:RoadLinkSequence) or //schema-element(tn-ra:RailwayLinkSequence)or //schema-element(tn-ca:CablewayLinkSequence) or //schema-element(tn-w:WaterLinkSequence) or //schema-element(tn-a:AirLinkSequence)
TransportLinkSet <a name="TransportLinkSet"></a> 	| 	//schema-element(tn-ro:Road) or //schema-element(tn-ro:ERoad) or //schema-element(tn-w:RailwayLine) or //schema-element(tn-ca:CablewayLinkSet) or //schema-element(tn-w:FerryCrossing) or //schema-element(tn-w:MarineWaterway) or //schema-element(tn-w:InlandWaterway) or //schema-element(tn-a:AirRoute)
TransportNode <a name="TransportNode"></a> 	| 	//schema-element(tn-ro:RoadNode) or //schema-element(tn-ra:RailwayNode) or //schema-element(tn-ra:RailwayYardNode) or //schema-element(tn-ra:RailwayStationNode) or //schema-element(tn-ca:CablewayNode) or //schema-element(tn-w:WaterwayNode) or //schema-element(tn-w:PortNode) or //schema-element(tn-a:Navaid) or //schema-element(tn-a:DesignatedPoint) or //schema-element(tn-a:RunwayCentrelinePoint) or //schema-element(tn-a:TouchDownLiftOff) or //schema-element(tn-a:AerodromeNode)
TransportPoint <a name="TransportPoint"></a> 	| 	//schema-element(tn:MarkerPost) or //schema-element(tn-w:Buoy) or //schema-element(tn-w:Beacon)
TransportProperty <a name="TransportProperty"></a> 	| 	//schema-element(tn:MaintenanceAuthority) or //schema-element(tn:OwnerAuthority) or //schema-element(tn:VerticalPosition) or //schema-element(tn:TrafficFlowDirection) or //schema-element(tn:ConditionOfFacility) or //schema-element(tn:RestrictionForVehicles) or //schema-element(tn:AccessRestriction) or //schema-element(tn-ro:FunctionalRoadClass) or //schema-element(tn-ro:RoadSurfaceCategory) or //schema-element(tn-ro:RoadServiceType) or //schema-element(tn-ro:RoadName) or //schema-element(tn-ro:NumberOfLanes) or //schema-element(tn-ro:SpeedLimit) or //schema-element(tn-ro:RoadWidth) or //schema-element(tn-ro:FormOfWay) or //schema-element(tn-ra:NominalTrackGauge) or //schema-element(tn-ra:RailwayElectrification) or //schema-element(tn-ra:RailwayType) or //schema-element(tn-ra:NumberOfTracks) or //schema-element(tn-ra:DesignSpeed) or //schema-element(tn-ra:RailwayUse) or //schema-element(tn-ra:RailwayStationCode) or //schema-element(tn-w:FerryUse) or //schema-element(tn-w:CEMTClass) or //schema-element(tn-w:RestrictionForWaterVehicles) or //schema-element(tn-w:WaterTrafficFlowDirection) or //schema-element(tn-w:ConditionOfWaterFacility) or //schema-element(tn-a:UpperAltitudeLimit) or //schema-element(tn-a:FieldElevation) or //schema-element(tn-a:LowerAltitudeLimit) or //schema-element(tn-a:AerodromeType) or //schema-element(tn-a:SurfaceComposition) or //schema-element(tn-a:useRestriction) or //schema-element(tn-a:ElementLength) or //schema-element(tn-a:ElementWidth) or //schema-element(tn-a:AerodromeCategory) or //schema-element(tn-a:ConditionOfAirFacility)
inspireID <a name="inspireID"></a> 	| 	//schema-element(tn:TrafficFlowDirection)/tn:inspireID or //schema-element(tn:TransportArea)/tn:inspireID or //schema-element(tn:TransportLink)/tn:inspireID or //schema-element(tn:TransportLinkSequence)/tn:inspireID or //schema-element(tn:TransportLinkSet)/tn:inspireID or //schema-element(tn:TransportNode)/tn:inspireID or //schema-element(tn:TransportPoint)/tn:inspireID or //schema-element(tn:TransportProperty)/tn:inspireID
link <a name="link"></a> 	| 	//schema-element(tn:TransportLinkSequence)/net:link/@href:xlink or //schema-element(tn:TransportLinkSet)/net:link/@href:xlink
inNetwork <a name="inNetwork"></a> 	| 	//schema-element(tn:TransportLinkSequence)/net:link/net:inNetwork/@href:xlink or //schema-element(tn:TransportLinkSet)/net:link/net:inNetwork/@href:xlink or //schema-element(tn:TransportLinkSequence)/net:inNetwork/@href:xlink or //schema-element(tn:TransportLinkSet)/net:inNetwork/@href:xlink
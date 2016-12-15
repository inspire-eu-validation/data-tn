# Object references

**Version**: 1

**Purpose**: Verify the consistent use of references to other features.

**Prerequisites**

**Test method**

* For each [NetworkProperty](#NetworkProperty) feature that links to a [TransportLink](#TransportLink) or a [TransportLinkSequence](#TransportLinkSequence), verify that any linear references are consistent with the length of the geometry of the network feature.
* For each [NetworkConnection](#NetworkConnection) with as value 'intermodal' for the [type attribute](#typeAttribute), verify that the two elements referenced in the [element association role](#elementAssociationRole) belong to different networks, i.e. they reference different networks in their [inNetwork association role](#inNetworkAssociationRole).

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-as/README#ref_TG_DS_tmpl) IR requirement Section 7.9.2 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-as/README#ref_TG_DS_tmpl) IR requirement Section 7.9.2 (2)

**Test type**: Automated

**Notes**:

## Messages

n/a

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
TransportProperty <a name="TransportProperty"></a> 	| 	//schema-element(tn:MaintenanceAuthority) or //schema-element(tn:OwnerAuthority) or //schema-element(tn:VerticalPosition) or //schema-element(tn:TrafficFlowDirection) or //schema-element(tn:ConditionOfFacility) or //schema-element(tn:RestrictionForVehicles) or //schema-element(tn:AccessRestriction) or //schema-element(tn-ro:FunctionalRoadClass) or //schema-element(tn-ro:RoadSurfaceCategory) or //schema-element(tn-ro:RoadServiceType) or //schema-element(tn-ro:RoadName) or //schema-element(tn-ro:NumberOfLanes) or //schema-element(tn-ro:SpeedLimit) or //schema-element(tn-ro:RoadWidth) or //schema-element(tn-ro:FormOfWay) or //schema-element(tn-ra:NominalTrackGauge) or //schema-element(tn-ra:RailwayElectrification) or //schema-element(tn-ra:RailwayType) or //schema-element(tn-ra:NumberOfTracks) or //schema-element(tn-ra:DesignSpeed) or //schema-element(tn-ra:RailwayUse) or //schema-element(tn-ra:RailwayStationCode) or //schema-element(tn-w:FerryUse) or //schema-element(tn-w:CEMTClass) or //schema-element(tn-w:RestrictionForWaterVehicles) or //schema-element(tn-w:WaterTrafficFlowDirection) or //schema-element(tn-w:ConditionOfWaterFacility) or //schema-element(tn-a:UpperAltitudeLimit) or //schema-element(tn-a:FieldElevation) or //schema-element(tn-a:LowerAltitudeLimit) or //schema-element(tn-a:AerodromeType) or //schema-element(tn-a:SurfaceComposition) or //schema-element(tn-a:useRestriction) or //schema-element(tn-a:ElementLength) or //schema-element(tn-a:ElementWidth) or //schema-element(tn-a:AerodromeCategory) or //schema-element(tn-a:ConditionOfAirFacility)
TransportLink <a name="TransportLink"></a> 	| 	//schema-element(tn-ro:RoadLink) or //schema-element(tn-ra:RailwayLink) or //schema-element(tn-ca:CablewayLink) or //schema-element(tn-w:WaterwayLink) or //schema-element(tn-a:AirRouteLink) or //schema-element(tn-a: ProcedureLink) or //schema-element(tn-a:StandardInstrumentDeparture) or //schema-element(tn-a:InstrumentApproachProcedure) or //schema-element(tn-a:StandardInstrumentArrival)
TransportLinkSequence <a name="TransportLinkSequence"></a> 	| 	//schema-element(tn-ro:RoadLinkSequence) or //schema-element(tn-ra:RailwayLinkSequence)or //schema-element(tn-ca:CablewayLinkSequence) or //schema-element(tn-w:WaterLinkSequence) or //schema-element(tn-a:AirLinkSequence)
NetworkConnection <a name="NetworkConnection"></a>	|	//schema-element(net:NetworkConnection)
type attribute <a name="typeAttribute"></a>	|	//schema-element(net:NetworkConnection)/net:type
element association role <a name="elementAssociationRole"></a>	|	//schema-element(net:NetworkConnection)/net:element/@xlink:href
inNetwork association role <a name="inNetworkAssociationRole"></a>	|	$NetworkElement/net:inNetwork
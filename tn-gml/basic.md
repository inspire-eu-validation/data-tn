# Basic test

**Version**: 1

**Purpose**: Verify that the spatial data set contains at least one Transport Networks feature.

**Prerequisites**

**Test method**

* Check that the set of [features](#features) in the spatial data set is not empty. Otherwise report [noFeature](#noFeature)

**Reference(s)**: 

* [TG DS-TN](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-gml/README#ref_TG_DS_AD) 5.4, 5.5

**Test type**: Automated

**Notes**

There is no requirement that we could reference in the Technical Guidelines, but such a requirement is clearly missing for any data set with Transport Networkses features. Maybe such a requirement should be added in the future revision?

## Messages

Identifier  |  Message text (parameters start with '$')
----------- | -------------------------------------------------------------------------
noFeature <a name="noFeature"/>  |  	The XML documents representing the spatial data set do not contain a feature of any of the spatial object types in the 'Transport Networkses' application schema. Therefore, the spatial data set cannot conform to this conformance class. If you have expected to find spatial objects from the application schema in the data set, please consult the statistics information to see the spatial object types that have been found.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-gml/README#namespaces).

Abbreviation                                          |  XPath expression
----------------------------------------------------- | ------------------------------------------------------------------
features <a name="features"></a>   |  schema-element(tn:AccessRestriction) \| //schema-element(tn:ConditionOfFacility) \| //schema-element(tn:MaintenanceAuthority) \| //schema-element(tn:MarkerPost) \| //schema-element(tn:OwnerAuthority) \| //schema-element(tn:RestrictionForVehicles) \| //schema-element(tn:TrafficFlowDirection) \| //schema-element(tn:TransportNetwork) \| //schema-element(tn:VerticalPosition) \| //schema-element(tn-ro:ERoad) \| //schema-element(tn-ro:FormOfWay) \| //schema-element(tn-ro:FunctionalRoadClass) \| //schema-element(tn-ro:NumberOfLanes) \| //schema-element(tn-ro:Road) \| //schema-element(tn-ro:RoadArea) \| //schema-element(tn-ro:RoadLink) \| //schema-element(tn-ro:RoadLinkSequence) \| //schema-element(tn-ro:RoadName) \| //schema-element(tn-ro:RoadNode) \| //schema-element(tn-ro:RoadServiceArea) \| //schema-element(tn-ro:RoadServiceType) \| //schema-element(tn-ro:RoadSurfaceCategory) \| //schema-element(tn-ro:RoadWidth) \| //schema-element(tn-ro:SpeedLimit) \| //schema-element(tn-ro:VehicleTrafficArea) \| //schema-element(tn-ra:DesignSpeed) \| //schema-element(tn-ra:NominalTrackGauge) \| //schema-element(tn-ra:NumberOfTracks) \| //schema-element(tn-ra:RailwayArea) \| //schema-element(tn-ra:RailwayElectrification) \| //schema-element(tn-ra:RailwayLine) \| //schema-element(tn-ra:RailwayLink) \| //schema-element(tn-ra:RailwayLinkSequence) \| //schema-element(tn-ra:RailwayNode) \| //schema-element(tn-ra:RailwayStationArea) \| //schema-element(tn-ra:RailwayStationCode) \| //schema-element(tn-ra:RailwayStationNode) \| //schema-element(tn-ra:RailwayType) \| //schema-element(tn-ra:RailwayUse) \| //schema-element(tn-ra:RailwayYardArea) \| //schema-element(tn-ra:RailwayYardNode) \| //schema-element(tn-c:CablewayLink) \| //schema-element(tn-c:CablewayLinkSequence) \| //schema-element(tn-c:CablewayLinkSet) \| //schema-element(tn-c:CablewayNode) \| //schema-element(tn-w:Beacon) \| //schema-element(tn-w:Buoy) \| //schema-element(tn-w:CEMTClass) \| //schema-element(tn-w:ConditionOfWaterFacility) \| //schema-element(tn-w:FairwayArea) \| //schema-element(tn-w:FerryCrossing) \| //schema-element(tn-w:FerryUse) \| //schema-element(tn-w:InlandWaterway) \| //schema-element(tn-w:MarineWaterway) \| //schema-element(tn-w:PortArea) \| //schema-element(tn-w:PortNode) \| //schema-element(tn-w:RestrictionForWaterVehicles) \| //schema-element(tn-w:TrafficSeparationSchemeCrossing) \| //schema-element(tn-w:TrafficSeparationSchemeLane) \| //schema-element(tn-w:TrafficSeparationSchemeRoundabout) \| //schema-element(tn-w:TrafficSeparationSchemeSeparator) \| //schema-element(tn-w:WaterLinkSequence) \| //schema-element(tn-w:WaterTrafficFlowDirection) \| //schema-element(tn-w:WaterwayLink) \| //schema-element(tn-w:WaterwayNode) \| //schema-element(tn-a:Type Package Stereotypes) \| //schema-element(tn-a:AerodromeArea) \| //schema-element(tn-a:AerodromeCategory) \| //schema-element(tn-a:AerodromeNode) \| //schema-element(tn-a:AerodromeType) \| //schema-element(tn-a:AirLinkSequence) \| //schema-element(tn-a:AirRoute) \| //schema-element(tn-a:AirRouteLink) \| //schema-element(tn-a:AirspaceArea) \| //schema-element(tn-a:ApronArea) \| //schema-element(tn-a:ConditionOfAirFacility) \| //schema-element(tn-a:DesignatedPoint) \| //schema-element(tn-a:ElementLength) \| //schema-element(tn-a:ElementWidth) \| //schema-element(tn-a:FieldElevation) \| //schema-element(tn-a:InstrumentApproachProcedure) \| //schema-element(tn-a:LowerAltitudeLimit) \| //schema-element(tn-a:Navaid) \| //schema-element(tn-a:ProcedureLink) \| //schema-element(tn-a:RunwayArea) \| //schema-element(tn-a:RunwayCentrelinePoint) \| //schema-element(tn-a:StandardInstrumentArrival) \| //schema-element(tn-a:StandardInstrumentDeparture) \| //schema-element(tn-a:SurfaceComposition) \| //schema-element(tn-a:TaxiwayArea) \| //schema-element(tn-a:TouchDownLiftOff) \| //schema-element(tn-a:UpperAltitudeLimit) \| //schema-element(tn-a:UseRestriction)

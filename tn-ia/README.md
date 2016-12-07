# Conformance class: Information accessibility, Transport Networks (DRAFT)

Conformance class for the requirements related to the accessibility of referenced information, for example, information stored in registries (code lists, coordinate reference systems).

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schema for Transport Networks".

This conformance class is part of the [Abstract Test Suite for the INSPIRE Data Specification on Transport Networks](http://inspire.ec.europa.eu/id/ats/data-tn/3.2).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the data set, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ia/README#ref_TG_DS_tmpl) | [Information accessibility](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/information-accessibility) | n/a |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-TN](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ia/README#ref_TG_DS_TN) | [GML application schema, Transport Networks - Network](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-gml) | INSPIRE spatial data set encoded in GML, Transport Networks features | n/a |
 
## Feature types <a name="feature-types"></a>

The instantiable feature types are:

Common:

* AccessRestriction
* ConditionOfFacility
* MaintenanceAuthority
* MarkerPost
* OwnerAuthority
* RestrictionForVehicles
* TrafficFlowDirection
* TransportNetwork
* VerticalPosition

Road Transport Networks:

* ERoad
* FormOfWay
* FunctionalRoadClass
* NumberOfLanes
* Road
* RoadArea
* RoadLink
* RoadLinkSequence
* RoadName
* RoadNode
* RoadServiceArea
* RoadServiceType
* RoadServiceCategory
* RoadWidth
* SpeedLimit
* VehicleTrafficArea

Rail Transport Networks:

* DesignSpeed
* NominalTrackGauge
* NumberOfTracks
* RailwayArea
* RailwayElectrification
* RailwayLine
* RailwayLink
* RailwayLinkSequence
* RailwayNode
* RailwayStationArea
* RailwayStationCode
* RailwayStationNode
* RailwayType
* RailwayUse
* RailwayYardArea
* RailwayYardNode

Cable Transport Networks:

* CablewayLink
* CablewayLinkSequence
* CablewayLinkSet
* CablewayNode

Water Transport Networks:

* Beacon
* Buoy
* CEMTClass
* ConditionOfWaterFacility
* FairwayArea
* FerryCrossing
* FerryUse
* InlandWaterway
* MarineWaterway
* PortArea
* PortNode
* RestrictionForWaterVehicles
* TrafficSeparationSchemeCrossing
* TrafficSeparationSchemeLane
* TrafficSeparationSchemeRoundabout
* TrafficSeparationSchemeSeparator
* WaterLinkSequence
* WaterTrafficFlowDirection
* WaterwayLink
* WaterwayNode

Air Transport Networks:

* Type Package Stereotypes
* AerodromeArea
* AerodromeCategory
* AerodromeNode
* AerodromeType
* AirLinkSequence
* AirRoute
* AirRouteLink
* AirspaceArea
* ApronArea
* ConditionOfAirFacility
* DesignatedPoint
* ElementLength
* ElementWidth
* FieldElevation
* InstrumentApproachProcedure
* LowerAltitudeLimit
* Navaid
* ProcedureLink
* RunwayArea
* RunwayCentrelinePoint
* StandardInstrumentArrival
* StandardInstrumentDeparture
* SurfaceComposition
* TaxiwayArea
* TouchDownLiftOff
* UpperAltitudeLimit
* UseRestriction

*Note*: When "features" or "spatial objects" are mentioned in the test cases, this refers only to instances of feature types of this application schema, not to any types specified in any other application schema.

## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
TG DS-tn <a name="ref_TG_DS_TN"></a>   | [INSPIRE Data Specification on Transport Networks – Technical Guidelines version 3.2](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_TN_v3.2.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-TN](#ref_TG_DS_TN)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Code lists](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ia/code-list)  | ready for review  | A.6.1 |
| [Feature references](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/hy-tn/features)  | ready for review  | A.1.4 |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         	| Namespace
-------------- 	| -------------------------------------------------
gml            	| http://www.opengis.net/gml/3.2
tn3            	| urn:x-inspire:specification:gmlas:CommonTransportElements:3.0
tn           	| http://inspire.ec.europa.eu/schemas/tn/4.0
tn-ro3			| urn:x-inspire:specification:gmlas:RoadTransportNetwork:3.0
tn-ro			| http://inspire.ec.europa.eu/schemas/tn-ro/4.0
tn-ra3			| urn:x-inspire:specification:gmlas:RailwayTransportNetwork:3.0
tn-ra			| http://inspire.ec.europa.eu/schemas/tn-ra/4.0
tn-c3			| urn:x-inspire:specification:gmlas:CableTransportNetwork:3.0
tn-c			| http://inspire.ec.europa.eu/schemas/tn-c/4.0
tn-w3			| urn:x-inspire:specification:gmlas:WaterTransportNetwork:3.0
tn-w			| http://inspire.ec.europa.eu/schemas/tn-w/4.0
tn-a3			| urn:x-inspire:specification:gmlas:AirTransportNetwork:3.0
tn-a			| http://inspire.ec.europa.eu/schemas/tn-a/4.0


The following variables are used to refer to the corresponding Xpath expressions in all test descriptions:

Variable       | Value
-------------- | -------------------------------------------------
$features      |  schema-element(tn:AccessRestriction) \| //schema-element(tn:ConditionOfFacility) \| //schema-element(tn:MaintenanceAuthority) \| //schema-element(tn:MarkerPost) \| //schema-element(tn:OwnerAuthority) \| //schema-element(tn:RestrictionForVehicles) \| //schema-element(tn:TrafficFlowDirection) \| //schema-element(tn:TransportNetwork) \| //schema-element(tn:VerticalPosition) \| //schema-element(tn-ro:ERoad) \| //schema-element(tn-ro:FormOfWay) \| //schema-element(tn-ro:FunctionalRoadClass) \| //schema-element(tn-ro:NumberOfLanes) \| //schema-element(tn-ro:Road) \| //schema-element(tn-ro:RoadArea) \| //schema-element(tn-ro:RoadLink) \| //schema-element(tn-ro:RoadLinkSequence) \| //schema-element(tn-ro:RoadName) \| //schema-element(tn-ro:RoadNode) \| //schema-element(tn-ro:RoadServiceArea) \| //schema-element(tn-ro:RoadServiceType) \| //schema-element(tn-ro:RoadServiceCategory) \| //schema-element(tn-ro:RoadWidth) \| //schema-element(tn-ro:SpeedLimit) \| //schema-element(tn-ro:VehicleTrafficArea) \| //schema-element(tn-ra:DesignSpeed) \| //schema-element(tn-ra:NominalTrackGauge) \| //schema-element(tn-ra:NumberOfTracks) \| //schema-element(tn-ra:RailwayArea) \| //schema-element(tn-ra:RailwayElectrification) \| //schema-element(tn-ra:RailwayLine) \| //schema-element(tn-ra:RailwayLink) \| //schema-element(tn-ra:RailwayLinkSequence) \| //schema-element(tn-ra:RailwayNode) \| //schema-element(tn-ra:RailwayStationArea) \| //schema-element(tn-ra:RailwayStationCode) \| //schema-element(tn-ra:RailwayStationNode) \| //schema-element(tn-ra:RailwayType) \| //schema-element(tn-ra:RailwayUse) \| //schema-element(tn-ra:RailwayYardArea) \| //schema-element(tn-ra:RailwayYardNode) \| //schema-element(tn-c:CablewayLink) \| //schema-element(tn-c:CablewayLinkSequence) \| //schema-element(tn-c:CablewayLinkSet) \| //schema-element(tn-c:CablewayNode) \| //schema-element(tn-w:Beacon) \| //schema-element(tn-w:Buoy) \| //schema-element(tn-w:CEMTClass) \| //schema-element(tn-w:ConditionOfWaterFacility) \| //schema-element(tn-w:FairwayArea) \| //schema-element(tn-w:FerryCrossing) \| //schema-element(tn-w:FerryUse) \| //schema-element(tn-w:InlandWaterway) \| //schema-element(tn-w:MarineWaterway) \| //schema-element(tn-w:PortArea) \| //schema-element(tn-w:PortNode) \| //schema-element(tn-w:RestrictionForWaterVehicles) \| //schema-element(tn-w:TrafficSeparationSchemeCrossing) \| //schema-element(tn-w:TrafficSeparationSchemeLane) \| //schema-element(tn-w:TrafficSeparationSchemeRoundabout) \| //schema-element(tn-w:TrafficSeparationSchemeSeparator) \| //schema-element(tn-w:WaterLinkSequence) \| //schema-element(tn-w:WaterTrafficFlowDirection) \| //schema-element(tn-w:WaterwayLink) \| //schema-element(tn-w:WaterwayNode) \| //schema-element(tn-a:Type Package Stereotypes) \| //schema-element(tn-a:AerodromeArea) \| //schema-element(tn-a:AerodromeCategory) \| //schema-element(tn-a:AerodromeNode) \| //schema-element(tn-a:AerodromeType) \| //schema-element(tn-a:AirLinkSequence) \| //schema-element(tn-a:AirRoute) \| //schema-element(tn-a:AirRouteLink) \| //schema-element(tn-a:AirspaceArea) \| //schema-element(tn-a:ApronArea) \| //schema-element(tn-a:ConditionOfAirFacility) \| //schema-element(tn-a:DesignatedPoint) \| //schema-element(tn-a:ElementLength) \| //schema-element(tn-a:ElementWidth) \| //schema-element(tn-a:FieldElevation) \| //schema-element(tn-a:InstrumentApproachProcedure) \| //schema-element(tn-a:LowerAltitudeLimit) \| //schema-element(tn-a:Navaid) \| //schema-element(tn-a:ProcedureLink) \| //schema-element(tn-a:RunwayArea) \| //schema-element(tn-a:RunwayCentrelinePoint) \| //schema-element(tn-a:StandardInstrumentArrival) \| //schema-element(tn-a:StandardInstrumentDeparture) \| //schema-element(tn-a:SurfaceComposition) \| //schema-element(tn-a:TaxiwayArea) \| //schema-element(tn-a:TouchDownLiftOff) \| //schema-element(tn-a:UpperAltitudeLimit) \| //schema-element(tn-a:UseRestriction)
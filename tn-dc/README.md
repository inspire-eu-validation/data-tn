# Conformance class: Data consistency, Transportation Networks (DRAFT)

Conformance class for the requirements related to the consistency of the data.

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schema, Transportation Networks Simple".

This conformance class is part of the [Abstract Test Suite for the INSPIRE Data Specification on Transportation Networks](http://inspire.ec.europa.eu/id/ats/data-tn/3.2).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the data set, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-dc/README#ref_TG_DS_tmpl) | [Data consistency](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/data-consistency) | n/a |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-TN](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-as/README#ref_TG_DS_TN) | [GML application schemas, Transportation Networks](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-gml) | INSPIRE spatial data set encoded in GML, Transportation Networks features | n/a |
 
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
TG DS-TN <a name="ref_TG_DS_TN"></a>   | [INSPIRE Data Specification on Transportation Networks – Technical Guidelines version 3.2](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_TN_v3.2.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-HY](#ref_TG_DS_HY)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Spatial consistency](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-dc/spatial)  | ready for review  | A.1.7, A.3.6  |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
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
gml            | http://www.opengis.net/gml/3.2

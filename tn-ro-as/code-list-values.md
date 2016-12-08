# Code list values

**Version**: 1

**Purpose**: Verify whether all attributes whose value type is a code list take the values set out therein

**Prerequisites**

**Test method**

When an attribute has a code list as its type, verify that the values comply with the definitions and include the values set out in Annex II of the regulation. To pass this tests that any instance of an attribute

* takes only values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'none'.

Otherwise report [disallowedCodeListValue](#disallowedCodeListValue).

In the Addresses application schema, the following properties have to be tested:
* [AreaConditionValue (v3)](#AreaConditionValue3). Valid values:
  * inNationalPark
  * insideCities
  * nearRailroadCrossing
  * nearSchool
  * outsideCities
  * trafficCalmingArea
* [AreaConditionValue (v4)](#AreaConditionValue4). Valid values:
  * http://inspire.ec.europa.eu/codelist/AreaConditionValue/inNationalPark
  * http://inspire.ec.europa.eu/codelist/AreaConditionValue/insideCities
  * http://inspire.ec.europa.eu/codelist/AreaConditionValue/nearRailroadCrossing
  * http://inspire.ec.europa.eu/codelist/AreaConditionValue/nearSchool
  * http://inspire.ec.europa.eu/codelist/AreaConditionValue/outsideCities
  * http://inspire.ec.europa.eu/codelist/AreaConditionValue/trafficCalmingArea
* [FormOfRoadNodeValue (v3)](#FormOfRoadNodeValue3). Valid values:
  * enclosedTrafficArea
  * junction
  * levelCrossing
  * pseudoNode
  * roadEnd
  * roadServiceArea
  * roundabout
  * trafficSquare
* [FormOfRoadNodeValue (v4)](#FormOfRoadNodeValue4). Valid values:
  * http://inspire.ec.europa.eu/codelist/FormOfRoadNodeValue/enclosedTrafficArea
  * http://inspire.ec.europa.eu/codelist/FormOfRoadNodeValue/junction
  * http://inspire.ec.europa.eu/codelist/FormOfRoadNodeValue/levelCrossing
  * http://inspire.ec.europa.eu/codelist/FormOfRoadNodeValue/pseudoNode
  * http://inspire.ec.europa.eu/codelist/FormOfRoadNodeValue/roadEnd
  * http://inspire.ec.europa.eu/codelist/FormOfRoadNodeValue/roadServiceArea
  * http://inspire.ec.europa.eu/codelist/FormOfRoadNodeValue/roundabout
  * http://inspire.ec.europa.eu/codelist/FormOfRoadNodeValue/trafficSquare
* [FormOfWayValue (v3)](#FormOfWayValue3). Valid values:
  * bicycleRoad
  * dualCarriageway
  * enclosedTrafficArea
  * entranceOrExitCarPark
  * entranceOrExitService
  * motorway
  * pedestrianZone
  * roundabout
  * serviceRoad
  * singleCarriageway
  * slipRoad
  * tractorRoad
  * trafficSquare
  * walkway
* [FormOfWayValue (v4)](#FormOfWayValue4). Valid values:
  * http://inspire.ec.europa.eu/codelist/FormOfWayValue/bicycleRoad
  * http://inspire.ec.europa.eu/codelist/FormOfWayValue/dualCarriageway
  * http://inspire.ec.europa.eu/codelist/FormOfWayValue/enclosedTrafficArea
  * http://inspire.ec.europa.eu/codelist/FormOfWayValue/entranceOrExitCarPark
  * http://inspire.ec.europa.eu/codelist/FormOfWayValue/entranceOrExitService
  * http://inspire.ec.europa.eu/codelist/FormOfWayValue/motorway
  * http://inspire.ec.europa.eu/codelist/FormOfWayValue/pedestrianZone
  * http://inspire.ec.europa.eu/codelist/FormOfWayValue/roundabout
  * http://inspire.ec.europa.eu/codelist/FormOfWayValue/serviceRoad
  * http://inspire.ec.europa.eu/codelist/FormOfWayValue/singleCarriageway
  * http://inspire.ec.europa.eu/codelist/FormOfWayValue/slipRoad
  * http://inspire.ec.europa.eu/codelist/FormOfWayValue/tractorRoad
  * http://inspire.ec.europa.eu/codelist/FormOfWayValue/trafficSquare
  * http://inspire.ec.europa.eu/codelist/FormOfWayValue/walkway
* [RoadPartValue (v3)](#RoadPartValue3). Valid values:
  * carriageway
  * pavedSurface
* [RoadPartValue (v4)](#RoadPartValue4). Valid values: 
  * http://inspire.ec.europa.eu/codelist/RoadPartValue/carriageway
  * http://inspire.ec.europa.eu/codelist/RoadPartValue/pavedSurface
 * [RoadServiceTypeValue (v3)](#RoadPartValue3). Valid values:
  * busStation
  * parking
  * restArea
  * toll
* [RoadServiceTypeValue (v4)](#RoadPartValue4). Valid values: 
  * http://inspire.ec.europa.eu/codelist/RoadServiceTypeValue/busStation
  * http://inspire.ec.europa.eu/codelist/RoadServiceTypeValue/parking
  * http://inspire.ec.europa.eu/codelist/RoadServiceTypeValue/restArea
  * http://inspire.ec.europa.eu/codelist/RoadServiceTypeValue/toll
 * [RoadSurfaceCategoryValue (v3)](#RoadSurfaceCategoryValue3). Valid values:
  * paved
  * unpaved
* [RoadSurfaceCategoryValue (v4)](#RoadSurfaceCategoryValue4). Valid values:
  * http://inspire.ec.europa.eu/codelist/RoadSurfaceCategoryValue/paved
  * http://inspire.ec.europa.eu/codelist/RoadSurfaceCategoryValue/unpaved
* [ServiceFacilityValue (v3)](#ServiceFacilityValue3). Valid values:
  * drinks
  * food
  * fuel
  * picnicArea
  * playground
  * shop
  * toilets
* [ServiceFacilityValue (v4)](#ServiceFacilityValue4). Valid values:
  * http://inspire.ec.europa.eu/codelist/ServiceFacilityValue/drinks
  * http://inspire.ec.europa.eu/codelist/ServiceFacilityValue/food
  * http://inspire.ec.europa.eu/codelist/ServiceFacilityValue/fuel
  * http://inspire.ec.europa.eu/codelist/ServiceFacilityValue/picnicArea
  * http://inspire.ec.europa.eu/codelist/ServiceFacilityValue/playground
  * http://inspire.ec.europa.eu/codelist/ServiceFacilityValue/shop
  * http://inspire.ec.europa.eu/codelist/ServiceFacilityValue/toilets
 * [SpeedLimitSourceValue (v3)](#SpeedLimitSourceValue3). Valid values:
  * fixedTrafficSign
  * regulation
  * variableTrafficSign
* [SpeedLimitSourceValue (v4)](#SpeedLimitSourceValue4). Valid values:
  * http://inspire.ec.europa.eu/codelist/SpeedLimitSourceValue/fixedTrafficSign
  * http://inspire.ec.europa.eu/codelist/SpeedLimitSourceValue/regulation
  * http://inspire.ec.europa.eu/codelist/SpeedLimitSourceValue/variableTrafficSign
 * [VehicleTypeValue (v3)](#VehicleTypeValue3). Valid values:
  * allVehicle
  * bicycle
  * carWithTrailer
  * deliveryTruck
  * emergencyVehicle
  * employeeVehicle
  * facilityVehicle
  * farmVehicle
  * highOccupancyVehicle
  * lightRail
  * mailVehicle
  * militaryVehicle
  * moped
  * motorcycle
  * passengerCar
  * pedestrian
  * privateBus
  * publicBus
  * residentialVehicle
  * schoolBus
  * snowChainEquippedVehicle
  * tanker
  * taxi
  * transportTruck
  * trolleyBus
  * vehicleForDisabledPerson
  * vehicleWithExplosiveLoad
  * vehicleWithOtherDangerousLoad
  * vehicleWithWaterPollutingLoad
* [VehicleTypeValue (v4)](#VehicleTypeValue4). Valid values:
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/allVehicle
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/bicycle
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/carWithTrailer
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/deliveryTruck
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/emergencyVehicle
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/employeeVehicle
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/facilityVehicle
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/farmVehicle
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/highOccupancyVehicle
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/lightRail
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/mailVehicle
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/militaryVehicle
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/moped
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/motorcycle
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/passengerCar
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/pedestrian
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/privateBus
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/publicBus
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/residentialVehicle
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/schoolBus
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/snowChainEquippedVehicle
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/tanker
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/taxi
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/transportTruck
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/trolleyBus
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/vehicleForDisabledPerson
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/vehicleWithExplosiveLoad
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/vehicleWithOtherDangerousLoad
  * http://inspire.ec.europa.eu/codelist/VehicleTypeValue/vehicleWithWaterPollutingLoad
 * [WeatherConditionValue (v3)](#WeatherConditionValue3). Valid values:
  * fog
  * ice
  * rain
  * smog
  * snow
* [WeatherConditionValue (v4)](#WeatherConditionValue4). Valid values:
  * http://inspire.ec.europa.eu/codelist/WeatherConditionValue/fog
  * http://inspire.ec.europa.eu/codelist/WeatherConditionValue/ice
  * http://inspire.ec.europa.eu/codelist/WeatherConditionValue/rain
  * http://inspire.ec.europa.eu/codelist/WeatherConditionValue/smog
  * http://inspire.ec.europa.eu/codelist/WeatherConditionValue/snow


The following is not applicable for this application schema as no extensions are allowed. It is still included here as a reminder in case extensions will be allowed in the future:

Inspect the code list valued property elements. If a value is not one of the values listed above, review the code list definition to check that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule and that all extensions conform to the requirements. This is a manual test.
  
**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ro-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ro-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (3)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ro-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ro-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (2)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ro-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (3)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ro-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (4)

**Test type**: Automated

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
disallowedCodeListValue <a name="disallowedCodeListValue"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that is not one of the allowed values listed at $codelist. 

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ro-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
AreaConditionValue (v3) <a name="AreaConditionValue3"></a>        | //schema-element(tn-ro3:
AreaConditionValue (v4) <a name="AreaConditionValue4"></a>        | //schema-element(tn-ro:
FormOfRoadNodeValue (v3) <a name="FormOfRoadNodeValue3"></a>      | //schema-element(tn-ro3:
FormOfRoadNodeValue (v4) <a name="FormOfRoadNodeValue4"></a>      | //schema-element(tn-ro:
FormOfWayValue (v3) <a name="FormOfWayValue3"></a>                | //schema-element(tn-ro3:
FormOfWayValue (v4) <a name="FormOfWayValue4"></a>                | //schema-element(tn-ro:
RoadPartValue (v3) <a name="RoadPartValue3"></a>                  | //schema-element(tn-ro3:
RoadPartValue (v4) <a name="RoadPartValue4"></a>                  | //schema-element(tn-ro:
RoadServiceTypeValue (v3) <a name="RoadPartValue3"></a>           | //schema-element(tn-ro3:
RoadServiceTypeValue (v4) <a name="RoadPartValue4"></a>           | //schema-element(tn-ro:
RoadSurfaceCategoryValue (v3) <a name="RoadSurfaceCategoryValue3"></a> | //schema-element(tn-ro3:
RoadSurfaceCategoryValue (v4) <a name="RoadSurfaceCategoryValue4"></a> | //schema-element(tn-ro:
ServiceFacilityValue (v3) <a name="ServiceFacilityValue3"></a>    | //schema-element(tn-ro3:
ServiceFacilityValue (v4) <a name="ServiceFacilityValue4"></a>    | //schema-element(tn-ro:
SpeedLimitSourceValue (v3) <a name="SpeedLimitSourceValue3"></a>  | //schema-element(tn-ro3:
SpeedLimitSourceValue (v4) <a name="SpeedLimitSourceValue4"></a>  | //schema-element(tn-ro:
VehicleTypeValue (v3) <a name="VehicleTypeValue3"></a>            | //schema-element(tn-ro3:
VehicleTypeValue (v4) <a name="VehicleTypeValue4"></a>            | //schema-element(tn-ro:
WeatherConditionValue (v3) <a name="WeatherConditionValue3"></a>  | //schema-element(tn-ro3:
WeatherConditionValue (v4) <a name="WeatherConditionValue4"></a>  | //schema-element(tn-ro:
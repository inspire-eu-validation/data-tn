# Constraints

**Version**: 1

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

Verify that the OCL constraints listed below that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation). 

For constraints that require retrieving a referenced resource and the resource cannot be retrieved, report [brokenLink](#brokenLink). The test accepts the following two types of content in @xlink:href attributes: Either a "#" followed by a @gml:id in the same document or a HTTP URI.

Automated tests:

* FormOfWay can only be associated with a spatial object that is part of a road transport network; OCL: "inv: networkRef.element.oclIsKindOf(Road) or networkRef.element.oclIsKindOf(ERoad) or networkRef.element.oclIsKindOf(RoadLink) or networkRef.element.oclIsKindOf(RoadLinkSequence) or networkRef.element.oclIsKindOf(RoadNode) or networkRef.element.oclIsKindOf(RoadArea) or networkRef.element.oclIsKindOf(RoadServiceArea) or networkRef.element.oclIsKindOf(VehicleTrafficArea)". Verify that a [FormOfWay](#FormOfWay) is only associated with a spatial object [Road](#Road), [ERoad](#ERoad), [RoadLink](#RoadLink), [RoadLinkSequence](#RoadLinkSequence), [RoadNode](#RoadNode), [RoadArea](#RoadArea), [RoadServiceArea](#RoadServiceArea), or [VehicleTrafficArea](#VehicleTrafficArea).
* FunctionalRoadClass can only be associated with a spatial object that is part of a road transport network; OCL: "inv: networkRef.element.oclIsKindOf(Road) or networkRef.element.oclIsKindOf(ERoad) or networkRef.element.oclIsKindOf(RoadLink) or networkRef.element.oclIsKindOf(RoadLinkSequence) or networkRef.element.oclIsKindOf(RoadNode) or networkRef.element.oclIsKindOf(RoadArea) or networkRef.element.oclIsKindOf(RoadServiceArea) or networkRef.element.oclIsKindOf(VehicleTrafficArea)". Verify that a [FunctionalRoadClass](#FunctionalRoadClass) is only associated with a spatial object [Road](#Road), [ERoad](#ERoad), [RoadLink](#RoadLink), [RoadLinkSequence](#RoadLinkSequence), [RoadNode](#RoadNode), [RoadArea](#RoadArea), [RoadServiceArea](#RoadServiceArea), or [VehicleTrafficArea](#VehicleTrafficArea).
* NumberOfLanes can only be associated with a spatial object that is part of a road transport network; OCL: "inv: networkRef.element.oclIsKindOf(Road) or networkRef.element.oclIsKindOf(ERoad) or networkRef.element.oclIsKindOf(RoadLink) or networkRef.element.oclIsKindOf(RoadLinkSequence) or networkRef.element.oclIsKindOf(RoadNode) or networkRef.element.oclIsKindOf(RoadArea) or networkRef.element.oclIsKindOf(RoadServiceArea) or networkRef.element.oclIsKindOf(VehicleTrafficArea)". Verify that a [NumberOfLanes](#NumberOfLanes) is only associated with a spatial object [Road](#Road), [ERoad](#ERoad), [RoadLink](#RoadLink), [RoadLinkSequence](#RoadLinkSequence), [RoadNode](#RoadNode), [RoadArea](#RoadArea), [RoadServiceArea](#RoadServiceArea), or [VehicleTrafficArea](#VehicleTrafficArea).
* RoadName can only be associated with a spatial object that is part of a road transport network; OCL: "inv: networkRef.element.oclIsKindOf(Road) or networkRef.element.oclIsKindOf(ERoad) or networkRef.element.oclIsKindOf(RoadLink) or networkRef.element.oclIsKindOf(RoadLinkSequence) or networkRef.element.oclIsKindOf(RoadNode) or networkRef.element.oclIsKindOf(RoadArea) or networkRef.element.oclIsKindOf(RoadServiceArea) or networkRef.element.oclIsKindOf(VehicleTrafficArea)". Verify that a [RoadName](#RoadName) is only associated with a spatial object [Road](#Road), [ERoad](#ERoad), [RoadLink](#RoadLink), [RoadLinkSequence](#RoadLinkSequence), [RoadNode](#RoadNode), [RoadArea](#RoadArea), [RoadServiceArea](#RoadServiceArea), or [VehicleTrafficArea](#VehicleTrafficArea).
* RoadSurfaceCategory can only be associated with a spatial object that is part of a road transport network; OCL: "inv: networkRef.element.oclIsKindOf(Road) or networkRef.element.oclIsKindOf(ERoad) or networkRef.element.oclIsKindOf(RoadLink) or networkRef.element.oclIsKindOf(RoadLinkSequence) or networkRef.element.oclIsKindOf(RoadNode) or networkRef.element.oclIsKindOf(RoadArea) or networkRef.element.oclIsKindOf(RoadServiceArea) or networkRef.element.oclIsKindOf(VehicleTrafficArea)". Verify that a [RoadSurfaceCategory](#RoadSurfaceCategory) is only associated with a spatial object [Road](#Road), [ERoad](#ERoad), [RoadLink](#RoadLink), [RoadLinkSequence](#RoadLinkSequence), [RoadNode](#RoadNode), [RoadArea](#RoadArea), [RoadServiceArea](#RoadServiceArea), or [VehicleTrafficArea](#VehicleTrafficArea).
* RoadWidth can only be associated with a spatial object that is part of a road transport network; OCL: "inv: networkRef.element.oclIsKindOf(Road) or networkRef.element.oclIsKindOf(ERoad) or networkRef.element.oclIsKindOf(RoadLink) or networkRef.element.oclIsKindOf(RoadLinkSequence) or networkRef.element.oclIsKindOf(RoadNode) or networkRef.element.oclIsKindOf(RoadArea) or networkRef.element.oclIsKindOf(RoadServiceArea) or networkRef.element.oclIsKindOf(VehicleTrafficArea)". Verify that a [RoadWidth](#RoadWidth) is only associated with a spatial object [Road](#Road), [ERoad](#ERoad), [RoadLink](#RoadLink), [RoadLinkSequence](#RoadLinkSequence), [RoadNode](#RoadNode), [RoadArea](#RoadArea), [RoadServiceArea](#RoadServiceArea), or [VehicleTrafficArea](#VehicleTrafficArea).
* SpeedLimit can only be associated with a spatial object that is part of a road transport network; OCL: "inv: networkRef.element.oclIsKindOf(Road) or networkRef.element.oclIsKindOf(ERoad) or networkRef.element.oclIsKindOf(RoadLink) or networkRef.element.oclIsKindOf(RoadLinkSequence) or networkRef.element.oclIsKindOf(RoadNode) or networkRef.element.oclIsKindOf(RoadArea) or networkRef.element.oclIsKindOf(RoadServiceArea) or networkRef.element.oclIsKindOf(VehicleTrafficArea)". Verify that a [SpeedLimit](#SpeedLimit) is only associated with a spatial object [Road](#Road), [ERoad](#ERoad), [RoadLink](#RoadLink), [RoadLinkSequence](#RoadLinkSequence), [RoadNode](#RoadNode), [RoadArea](#RoadArea), [RoadServiceArea](#RoadServiceArea), or [VehicleTrafficArea](#VehicleTrafficArea).
* RoadServiceType can only be associated with a spatial object of the type RoadServiceArea or RoadNode (when formOfRoadNode=roadServiceArea); OCL: "inv: networkRef.element.oclIsKindOf(RoadServiceArea) or (networkRef.element.oclIsKindOf(RoadNode) and networkRef.element.formOfRoadNode = FormOfRoadNodeValue::roadServiceArea)". Verify that a [RoadServiceType](#RoadServiceType) is only associated with a spatioal object [RoadServiceArea](#RoadServiceArea), or [RoadNode](#RoadNode) when the attribute [formOfRoadNode](#formOfRoadNode) has roadServiceArea as value.

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-a-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-TN](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-a-as/README#ref_TG_DS_TN)) 5.4

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-a-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
FormOfWay <a name="FormOfWay"></a> 						| 	//schema-element(tn-ro:
FunctionalRoadClass <a name="FunctionalRoadClass"></a> 	| 	//schema-element(tn-ro:
NumberOfLanes <a name="NumberOfLanes"></a> 				| 	//schema-element(tn-ro:
RoadName <a name="RoadName"></a> 						| 	//schema-element(tn-ro:
RoadSurfaceCategory <a name="RoadSurfaceCategory"></a> 	| 	//schema-element(tn-ro:
RoadWidth <a name="RoadWidth"></a> 						| 	//schema-element(tn-ro:
SpeedLimit <a name="SpeedLimit"></a> 					| 	//schema-element(tn-ro:
Road <a name="Road"></a> 								| 	//schema-element(tn-ro:
ERoad <a name="ERoad"></a> 								| 	//schema-element(tn-ro:
RoadLink <a name="RoadLink"></a> 						| 	//schema-element(tn-ro:
RoadLinkSequence <a name="RoadLinkSequence"></a> 		| 	//schema-element(tn-ro:
RoadNode <a name="RoadNode"></a> 						| 	//schema-element(tn-ro:
RoadArea <a name="RoadArea"></a> 						| 	//schema-element(tn-ro:
RoadServiceArea <a name="RoadServiceArea"></a> 			| 	//schema-element(tn-ro:
VehicleTrafficArea <a name="VehicleTrafficArea"></a> 	| 	//schema-element(tn-ro:
RoadServiceType <a name="RoadServiceType"></a> 			| 	//schema-element(tn-ro:
RoadServiceArea <a name="RoadServiceArea"></a> 			| 	//schema-element(tn-ro:
RoadNode <a name="RoadNode"></a> 						| 	//schema-element(tn-ro:
formOfRoadNode <a name="formOfRoadNode"></a> 			| 	//schema-element(tn-ro:

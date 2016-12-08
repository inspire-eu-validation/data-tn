# Constraints

**Version**: 1

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

Verify that the OCL constraints listed below that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation). 

For constraints that require retrieving a referenced resource and the resource cannot be retrieved, report [brokenLink](#brokenLink). The test accepts the following two types of content in @xlink:href attributes: Either a "#" followed by a @gml:id in the same document or a HTTP URI.

Automated tests:

* CEMTClass can only be associated with a spatial object that is part of a water transport network; OCL: "inv: networkRef.element.oclIsKindOf(InlandWaterway)". Verify that a [CEMTClass](#CEMTClass) is only associated with a spatial object [InlandWaterway](#InlandWaterway).
* ConditionOfWaterFacility can only be associated with a spatial object that is part of a water transport network; OCL: "inv: networkRef.element.oclIsKindOf(PortArea) or networkRef.element.oclIsKindOf(PortNode)". Verify that a [ConditionOfWaterFacility](#ConditionOfWaterFacility) is only associated with a spatial object [PortArea](#PortArea) or [PortNode](#PortNode).
* FerryUse can only be associated with a spatial object that is part of a water transport network; OCL: "inv: networkRef.element.oclIsKindOf(FerryCrossing)". Verify that a [FerryUse](#FerryUse) is only associated with a spatial object [FerryCrossing](#FerryCrossing).
* RestrictionForWaterVehicles can only be associated with a spatial object that is part of a water transport network; OCL: "inv: networkRef.element.oclIsKindOf(WaterwayLink) or networkRef.element.oclIsKindOf(WaterwayNode)". Verify that a [RestrictionForWaterVehicles](#RestrictionForWaterVehicles) is only associated with a spatial object [WaterwayLink](#WaterwayLink) or [WaterwayNode](#WaterwayNode).
* WaterTrafficFlowDirection can only be associated with a spatial object that is part of a water transport network; OCL: "inv: networkRef.element.oclIsKindOf(WaterLinkSequence) or networkRef.element.oclIsKindOf(WaterwayLink)". Verify that a [WaterTrafficFlowDirection](#WaterTrafficFlowDirection) is only associated with a spatial object [WaterLinkSequence](#WaterLinkSequence) or [WaterwayLink](#WaterwayLink).


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
CEMTClass <a name="CEMTClass"></a> 							| 	//schema-element(
InlandWaterway <a name="InlandWaterway"></a> 				| 	//schema-element(
ConditionOfWaterFacility <a name="ConditionOfWaterFacility"></a> | //schema-element(
PortArea <a name="PortArea"></a> 							| 	//schema-element(
PortNode <a name="PortNode"></a> 							| 	//schema-element(
FerryUse <a name="FerryUse"></a> 							| 	//schema-element(
FerryCrossing <a name="FerryCrossing"></a> 					| 	//schema-element(
RestrictionForWaterVehicles <a name="RestrictionForWaterVehicles"></a> | //schema-element(
WaterwayLink <a name="WaterwayLink"></a> 					| 	//schema-element(
WaterwayNode <a name="WaterwayNode"></a> 					| 	//schema-element(
WaterTrafficFlowDirection <a name="WaterTrafficFlowDirection"></a> | //schema-element(
WaterLinkSequence <a name="WaterLinkSequence"></a> 			| 	//schema-element(
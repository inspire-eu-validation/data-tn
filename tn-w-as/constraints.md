# Constraints

**Version**: 1

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

Verify that the OCL constraints listed below that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation). 

For constraints that require retrieving a referenced resource and the resource cannot be retrieved, report [brokenLink](#brokenLink). The test accepts the following two types of content in @xlink:href attributes: Either a "#" followed by a @gml:id in the same document or a HTTP URI.

Automated tests:

* CEMTClass can only be associated with a spatial object that is part of a water transport network; OCL: "inv: networkRef.element.oclIsKindOf(InlandWaterway)". Verify that a [CEMTClass](#CEMTClass) only has a [Network element association](#NetworkElement1) with a spatial object InlandWaterway.
* ConditionOfWaterFacility can only be associated with a spatial object that is part of a water transport network; OCL: "inv: networkRef.element.oclIsKindOf(PortArea) or networkRef.element.oclIsKindOf(PortNode)". Verify that a [ConditionOfWaterFacility](#ConditionOfWaterFacility) only has a [Network element association](#NetworkElement2) with a spatial object PortArea or PortNode.
* FerryUse can only be associated with a spatial object that is part of a water transport network; OCL: "inv: networkRef.element.oclIsKindOf(FerryCrossing)". Verify that a [FerryUse](#FerryUse) only has a [Network element association](#NetworkElement3) with a spatial object FerryCrossing.
* RestrictionForWaterVehicles can only be associated with a spatial object that is part of a water transport network; OCL: "inv: networkRef.element.oclIsKindOf(WaterwayLink) or networkRef.element.oclIsKindOf(WaterwayNode)". Verify that a [RestrictionForWaterVehicles](#RestrictionForWaterVehicles) only has a [Network element association](#NetworkElement4) with a spatial object WaterwayLink or WaterwayNode.
* WaterTrafficFlowDirection can only be associated with a spatial object that is part of a water transport network; OCL: "inv: networkRef.element.oclIsKindOf(WaterLinkSequence) or networkRef.element.oclIsKindOf(WaterwayLink)". Verify that a [WaterTrafficFlowDirection](#WaterTrafficFlowDirection) only has a [Network element association](#NetworkElement5) with a spatial object WaterLinkSequence or WaterwayLink.


**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-w-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-TN](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-w-as/README#ref_TG_DS_TN) 5.4

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-w-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
CEMTClass <a name="CEMTClass"></a> 														| //schema-element(tn-w:CEMTClass)
Network element association CEMTClass <a name="NetworkElement1"></a>   					| //schema-element(tn-w:CEMTClass)/net:networkRef/*/net:element/@xlink:href 
ConditionOfWaterFacility <a name="ConditionOfWaterFacility"></a> 						| //schema-element(tn-w:ConditionOfWaterFacility)
Network element association ConditionOfWaterFacility <a name="NetworkElement2"></a>   	| //schema-element(tn-w:ConditionOfWaterFacility)/net:networkRef/*/net:element/@xlink:href 
FerryUse <a name="FerryUse"></a> 														| //schema-element(tn-w:FerryUse)
Network element association FerryUse <a name="NetworkElement3"></a>   					| //schema-element(tn-w:FerryUse)/net:networkRef/*/net:element/@xlink:href 
RestrictionForWaterVehicles <a name="RestrictionForWaterVehicles"></a> 					| //schema-element(tn-w:RestrictionForWaterVehicles)
Network element association RestrictionForWaterVehicles <a name="NetworkElement4"></a>  | //schema-element(tn-w:RestrictionForWaterVehicles)/net:networkRef/*/net:element/@xlink:href 
WaterTrafficFlowDirection <a name="WaterTrafficFlowDirection"></a> 						| //schema-element(tn-w:WaterTrafficFlowDirection)
Network element association WaterTrafficFlowDirection <a name="NetworkElement5"></a>   	| //schema-element(tn-w:WaterTrafficFlowDirection)/net:networkRef/*/net:element/@xlink:href 
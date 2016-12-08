# Constraints

**Version**: 1

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

Verify that the OCL constraints listed below that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation). 

For constraints that require retrieving a referenced resource and the resource cannot be retrieved, report [brokenLink](#brokenLink). The test accepts the following two types of content in @xlink:href attributes: Either a "#" followed by a @gml:id in the same document or a HTTP URI.

Automated tests:

* FormOfWay can only be associated with a spatial object that is part of a road transport network; OCL: "inv: networkRef.element.oclIsKindOf(Road) or networkRef.element.oclIsKindOf(ERoad) or networkRef.element.oclIsKindOf(RoadLink) or networkRef.element.oclIsKindOf(RoadLinkSequence) or networkRef.element.oclIsKindOf(RoadNode) or networkRef.element.oclIsKindOf(RoadArea) or networkRef.element.oclIsKindOf(RoadServiceArea) or networkRef.element.oclIsKindOf(VehicleTrafficArea)". Verify that a [FormOfWay](#FormOfWay) only has a [Network element association](#NetworkElement1) with a spatial object Road, ERoad, RoadLink, RoadLinkSequence, RoadNode, RoadArea, RoadServiceArea, or VehicleTrafficArea.
* FunctionalRoadClass can only be associated with a spatial object that is part of a road transport network; OCL: "inv: networkRef.element.oclIsKindOf(Road) or networkRef.element.oclIsKindOf(ERoad) or networkRef.element.oclIsKindOf(RoadLink) or networkRef.element.oclIsKindOf(RoadLinkSequence) or networkRef.element.oclIsKindOf(RoadNode) or networkRef.element.oclIsKindOf(RoadArea) or networkRef.element.oclIsKindOf(RoadServiceArea) or networkRef.element.oclIsKindOf(VehicleTrafficArea)". Verify that a [FunctionalRoadClass](#FunctionalRoadClass) only has a [Network element association](#NetworkElement2) with a spatial object Road, ERoad, RoadLink, RoadLinkSequence, RoadNode, RoadArea, RoadServiceArea, or VehicleTrafficArea.
* NumberOfLanes can only be associated with a spatial object that is part of a road transport network; OCL: "inv: networkRef.element.oclIsKindOf(Road) or networkRef.element.oclIsKindOf(ERoad) or networkRef.element.oclIsKindOf(RoadLink) or networkRef.element.oclIsKindOf(RoadLinkSequence) or networkRef.element.oclIsKindOf(RoadNode) or networkRef.element.oclIsKindOf(RoadArea) or networkRef.element.oclIsKindOf(RoadServiceArea) or networkRef.element.oclIsKindOf(VehicleTrafficArea)". Verify that a [NumberOfLanes](#NumberOfLanes) only has a [Network element association](#NetworkElement3) with a spatial object Road, ERoad, RoadLink, RoadLinkSequence, RoadNode, RoadArea, RoadServiceArea, or VehicleTrafficArea.
* RoadName can only be associated with a spatial object that is part of a road transport network; OCL: "inv: networkRef.element.oclIsKindOf(Road) or networkRef.element.oclIsKindOf(ERoad) or networkRef.element.oclIsKindOf(RoadLink) or networkRef.element.oclIsKindOf(RoadLinkSequence) or networkRef.element.oclIsKindOf(RoadNode) or networkRef.element.oclIsKindOf(RoadArea) or networkRef.element.oclIsKindOf(RoadServiceArea) or networkRef.element.oclIsKindOf(VehicleTrafficArea)". Verify that a [RoadName](#RoadName) only has a [Network element association](#NetworkElement4) with a spatial object Road, ERoad, RoadLink, RoadLinkSequence, RoadNode, RoadArea, RoadServiceArea, or VehicleTrafficArea.
* RoadSurfaceCategory can only be associated with a spatial object that is part of a road transport network; OCL: "inv: networkRef.element.oclIsKindOf(Road) or networkRef.element.oclIsKindOf(ERoad) or networkRef.element.oclIsKindOf(RoadLink) or networkRef.element.oclIsKindOf(RoadLinkSequence) or networkRef.element.oclIsKindOf(RoadNode) or networkRef.element.oclIsKindOf(RoadArea) or networkRef.element.oclIsKindOf(RoadServiceArea) or networkRef.element.oclIsKindOf(VehicleTrafficArea)". Verify that a [RoadSurfaceCategory](#RoadSurfaceCategory) only has a [Network element association](#NetworkElement5) with a spatial object Road, ERoad, RoadLink, RoadLinkSequence, RoadNode, RoadArea, RoadServiceArea, or VehicleTrafficArea.
* RoadWidth can only be associated with a spatial object that is part of a road transport network; OCL: "inv: networkRef.element.oclIsKindOf(Road) or networkRef.element.oclIsKindOf(ERoad) or networkRef.element.oclIsKindOf(RoadLink) or networkRef.element.oclIsKindOf(RoadLinkSequence) or networkRef.element.oclIsKindOf(RoadNode) or networkRef.element.oclIsKindOf(RoadArea) or networkRef.element.oclIsKindOf(RoadServiceArea) or networkRef.element.oclIsKindOf(VehicleTrafficArea)". Verify that a [RoadWidth](#RoadWidth) only has a [Network element association](#NetworkElement6) with a spatial object Road, ERoad, RoadLink, RoadLinkSequence, RoadNode, RoadArea, RoadServiceArea, or VehicleTrafficArea.
* SpeedLimit can only be associated with a spatial object that is part of a road transport network; OCL: "inv: networkRef.element.oclIsKindOf(Road) or networkRef.element.oclIsKindOf(ERoad) or networkRef.element.oclIsKindOf(RoadLink) or networkRef.element.oclIsKindOf(RoadLinkSequence) or networkRef.element.oclIsKindOf(RoadNode) or networkRef.element.oclIsKindOf(RoadArea) or networkRef.element.oclIsKindOf(RoadServiceArea) or networkRef.element.oclIsKindOf(VehicleTrafficArea)". Verify that a [SpeedLimit](#SpeedLimit) only has a [Network element association](#NetworkElement7) with a spatial object Road, ERoad, RoadLink, RoadLinkSequence, RoadNode, RoadArea, RoadServiceArea, or VehicleTrafficArea.
* RoadServiceType can only be associated with a spatial object of the type RoadServiceArea or RoadNode (when formOfRoadNode=roadServiceArea); OCL: "inv: networkRef.element.oclIsKindOf(RoadServiceArea) or (networkRef.element.oclIsKindOf(RoadNode) and networkRef.element.formOfRoadNode = FormOfRoadNodeValue::roadServiceArea)". Verify that a [RoadServiceType](#RoadServiceType) only has a [Network element association](#NetworkElement8) with a spatial object RoadServiceArea, or RoadNode when the attribute [formOfRoadNode](#formOfRoadNode) has roadServiceArea as value.

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ro-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-TN](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ro-as/README#ref_TG_DS_TN)) 5.4

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ro-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
FormOfWay <a name="FormOfWay"></a> 												| //schema-element(tn-ro:FormOfWay)
Network element association FormOfWay <a name="NetworkElement1"></a>   			| //schema-element(tn-ro:FormOfWay)/net:networkRef/*/net:element/@xlink:href 
FunctionalRoadClass <a name="FunctionalRoadClass"></a> 							| //schema-element(tn-ro:FunctionalRoadClass)
Network element association FunctionalRoadClass <a name="NetworkElement2"></a>  | //schema-element(tn-ro:FunctionalRoadClass)/net:networkRef/*/net:element/@xlink:href 
NumberOfLanes <a name="NumberOfLanes"></a> 										| //schema-element(tn-ro:NumberOfLanes)
Network element association NumberOfLanes <a name="NetworkElement3"></a>   		| //schema-element(tn-ro:NumberOfLanes)/net:networkRef/*/net:element/@xlink:href 
RoadName <a name="RoadName"></a> 												| //schema-element(tn-ro:RoadName)
Network element association RoadName <a name="NetworkElement4"></a>   			| //schema-element(tn-ro:RoadName)/net:networkRef/*/net:element/@xlink:href 
RoadSurfaceCategory <a name="RoadSurfaceCategory"></a> 							| //schema-element(tn-ro:RoadSurfaceCategory)
Network element association RoadSurfaceCategory <a name="NetworkElement5"></a>  | //schema-element(tn-ro:RoadSurfaceCategory)/net:networkRef/*/net:element/@xlink:href 
RoadWidth <a name="RoadWidth"></a> 												| //schema-element(tn-ro:RoadWidth)
Network element association RoadWidth <a name="NetworkElement6"></a>   			| //schema-element(tn-ro:RoadWidth)/net:networkRef/*/net:element/@xlink:href 
SpeedLimit <a name="SpeedLimit"></a> 											| //schema-element(tn-ro:SpeedLimit)
Network element association SpeedLimit <a name="NetworkElement7"></a>   		| //schema-element(tn-ro:SpeedLimit)/net:networkRef/*/net:element/@xlink:href 
RoadServiceType <a name="RoadServiceType"></a> 									| //schema-element(tn-ro:RoadServiceType)
Network element association RoadServiceType <a name="NetworkElement8"></a>   	| //schema-element(tn-ro:RoadServiceType)/net:networkRef/*/net:element/@xlink:href 
formOfRoadNode attribute of RoadNode <a name="formOfRoadNode"></a> 				| //schema-element(tn-ro:RoadNode)/tn-ro:formOfRoadNode

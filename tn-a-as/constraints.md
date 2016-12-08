# Constraints

**Version**: 1

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

Verify that the OCL constraints listed below that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation). 

For constraints that require retrieving a referenced resource and the resource cannot be retrieved, report [brokenLink](#brokenLink). The test accepts the following two types of content in @xlink:href attributes: Either a "#" followed by a @gml:id in the same document or a HTTP URI.

Automated tests:

* AerodromeCategory can only be associated with a spatial object that is an Aerodrome Node or an Aerodrome Area; OCL: "inv: networkRef.element.oclIsKindOf(AerodromeNode) or networkRef.element.oclIsKindOf(AerodromeArea)". Verify that an [AerodromeCategory](#AerodromeCategory)  only has a [Network element association](#NetworkElement1) with a spatial object AerodromeNode or AerodromeArea.
* AerodromeType can only be associated with a spatial object that is an Aerodrome Node or Aerodrome Area; OCL: "inv: networkRef.element.oclIsKindOf(AerodromeNode) or networkRef.element.oclIsKindOf(AerodromeArea)". Verify that an [AerodromeType](#AerodromeType)  only has a [Network element association](#NetworkElement2) with a spatial object AerodromeNode or AerodromeArea.
* ConditionOfAirFacility can only be associated with a spatial object that is an Aerodrome Node, an Aerodrome Area or a Runway Area; OCL: "inv: networkRef.element.oclIsKindOf(AerodromeNode) or networkRef.element.oclIsKindOf(AerodromeArea) or networkRef.element.oclIsKindOf(RunwayArea)". Verify that a [ConditionOfAirFacility](#ConditionOfAirFacility)  only has a [Network element association](#NetworkElement3) with a spatial object AerodromeNode, AerodromeArea or RunwayArea.
* ElementLength can only be associated with a spatial object that is a Runway Area, Taxiway Area or Touch Down Lift Off; OCL: "inv: networkRef.element.oclIsKindOf(RunwayArea) or networkRef.element.oclIsKindOf(TaxiwayArea) or networkRef.element.oclIsKindOf(TouchDownLiftOff)." Verify that an [ElementLength](#ElementLength)  only has a [Network element association](#NetworkElement4) with a spatial object RunwayArea, TaxiwayArea or TouchDownLiftOff.
* ElementWidth can only be associated with a spatial object that is a Runway Area, Taxiway Area or Touch Down Lift Off; OCL: "inv: networkRef.element.oclIsKindOf(RunwayArea) or networkRef.element.oclIsKindOf(TaxiwayArea) or networkRef.element.oclIsKindOf(TouchDownLiftOff)". Verify that an [ElementWidth](#ElementWidth)  only has a [Network element association](#NetworkElement5) with a spatial object RunwayArea, TaxiwayArea or TouchDownLiftOff.
* FieldElevation can only be associated with a spatial object that is an Aerodrome Node or Aerodrome Area; OCL: "inv: networkRef.element.oclIsKindOf(AerodromeNode) or networkRef.element.oclIsKindOf(AerodromeArea)". Verify that a [FieldElevation](#FieldElevation)  only has a [Network element association](#NetworkElement6) with a spatial object AerodromeNode or AerodromeArea.
* LowerAltitudeLimit can only be associated with a spatial object that is an Air Route Link or Airspace Area; OCL: "inv: networkRef.element.oclIsKindOf(AirRouteLink) or networkRef.element.oclIsKindOf(AirspaceArea)". Verify that a [LowerAltitudeLimit](#LowerAltitudeLimit)  only has a [Network element association](#NetworkElement7) with a spatial object AirRouteLink or AirspaceArea.
* SurfaceComposition can only be associated with a spatial object that is a Runway Area, Taxiway Area, Apron Area or Touch Down Lift Off; OCL: "inv: networkRef.element.oclIsKindOf(RunwayArea) or networkRef.element.oclIsKindOf(TaxiwayArea) or networkRef.element.oclIsKindOf(ApronArea) or networkRef.element.oclIsKindOf(TouchDownLiftOff)". Verify that a [SurfaceComposition](#SurfaceComposition)  only has a [Network element association](#NetworkElement8) with a spatial object RunwayArea, TaxiwayArea, ApronArea or TouchDownLiftOff.
* UpperAltitudeLimit can only be associated with a spatial object that is an Air Route Link or Airspace Area; OCL: "inv: networkRef.element.oclIsKindOf(AirRouteLink) or networkRef.element.oclIsKindOf(AirspaceArea)". Verify that an [UpperAltitudeLimit](#UpperAltitudeLimit)  only has a [Network element association](#NetworkElement9) with a spatial object AirRouteLink or AirspaceArea.
* UseRestriction can only be associated with a spatial object that is an Air Route, Air Link (or specialized Air Link), Air Node (or specialized Air Node) or Aerodrome Area; OCL: "inv: networkRef.element.oclIsKindOf(AirRoute) or networkRef.element.oclIsKindOf(AirLink) or networkRef.element.oclIsKindOf(AirNode) or networkRef.element.oclIsKindOf(AerodromeArea)". Verify that a [UseRestriction](#UseRestriction)  only has a [Network element association](#NetworkElement10) with a spatial object AirRoute, AirLink, AirNode or AerodromeArea.

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-a-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-TN](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-a-as/README#ref_TG_DS_TN) 5.4

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
AerodromeCategory <a name="AerodromeCategory"></a> 								| //schema-element(tn-a:AerodromeCategory) 
Network element association AerodromeCategory <a name="NetworkElement1"></a>   	| //schema-element(tn-a:AerodromeCategory)/net:networkRef/*/net:element/@xlink:href
AerodromeType <a name="AerodromeType"></a> 										| //schema-element(tn-a:AerodromeType) 
Network element association AerodromeType <a name="NetworkElement2"></a>   		| //schema-element(tn-a:AerodromeType)/net:networkRef/*/net:element/@xlink:href 
ConditionOfAirFacility <a name="ConditionOfAirFacility"></a> 					| //schema-element(tn-a:ConditionOfAirFacility) 
Network element association ConditionOfAirFacility <a name="NetworkElement3"></a> | //schema-element(tn-a:ConditionOfAirFacility)/net:networkRef/*/net:element/@xlink:href 
ElementLength <a name="ElementLength"></a> 										| //schema-element(tn-a:ElementLength) 
Network element association ElementLength <a name="NetworkElement4"></a>   		| //schema-element(tn-a:ElementLength)/net:networkRef/*/net:element/@xlink:href 
ElementWidth <a name="ElementWidth"></a> 										| //schema-element(tn-a:ElementWidth) 
Network element association ElementWidth <a name="NetworkElement5"></a>   		| //schema-element(tn-a:ElementWidth)/net:networkRef/*/net:element/@xlink:href 
FieldElevation <a name="FieldElevation"></a> 									| //schema-element(tn-a:FieldElevation) 
Network element association FieldElevation <a name="NetworkElement6"></a> 	 	| //schema-element(tn-a:FieldElevation)/net:networkRef/*/net:element/@xlink:href 
LowerAltitudeLimit <a name="LowerAltitudeLimit"></a> 							| //schema-element(tn-a:LowerAltitudeLimit) 
Network element association LowerAltitudeLimit <a name="NetworkElement7"></a>   | //schema-element(tn-a:LowerAltitudeLimit)/net:networkRef/*/net:element/@xlink:href 
SurfaceComposition <a name="SurfaceComposition"></a> 							| //schema-element(tn-a:SurfaceComposition) 
Network element association SurfaceComposition <a name="NetworkElement8"></a>   | //schema-element(tn-a:SurfaceComposition)/net:networkRef/*/net:element/@xlink:href 
UpperAltitudeLimit <a name="UpperAltitudeLimit"></a> 							| //schema-element(tn-a:UpperAltitudeLimit) 
Network element association UpperAltitudeLimit <a name="NetworkElement9"></a>   | //schema-element(tn-a:UpperAltitudeLimit)/net:networkRef/*/net:element/@xlink:href 
UseRestriction <a name="UseRestriction"></a> 									| //schema-element(tn-a:UseRestriction) 
Network element association UseRestriction <a name="NetworkElement10"></a>   	| //schema-element(tn-a:UseRestriction)/net:networkRef/*/net:element/@xlink:href
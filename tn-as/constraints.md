# Constraints

**Version**: 1

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

Verify that the OCL constraints listed below that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation). 

For constraints that require retrieving a referenced resource and the resource cannot be retrieved, report [brokenLink](#brokenLink). The test accepts the following two types of content in @xlink:href attributes: Either a "#" followed by a @gml:id in the same document or a HTTP URI.

Automated tests:

* AerodromeCategory can only be associated with a spatial object that is an Aerodrome Node or an Aerodrome Area; OCL: "inv: networkRef.element.oclIsKindOf(AerodromeNode) or networkRef.element.oclIsKindOf(AerodromeArea)". Verify that an [AerodromeCategory](#AerodromeCategory) is only associated with a spatial object [AerodromeNode](#AerodromeNode) or [AerodromeArea](#AerodromeArea).
* AerodromeType can only be associated with a spatial object that is an Aerodrome Node or Aerodrome Area; OCL: "inv: networkRef.element.oclIsKindOf(AerodromeNode) or networkRef.element.oclIsKindOf(AerodromeArea)". Verify that an [AerodromeType](#AerodromeType) is only associated with a spatial object [AerodromeNode](#AerodromeNode) or [AerodromeArea](#AerodromeArea).
* ConditionOfAirFacility can only be associated with a spatial object that is an Aerodrome Node, an Aerodrome Area or a Runway Area; OCL: "inv: networkRef.element.oclIsKindOf(AerodromeNode) or networkRef.element.oclIsKindOf(AerodromeArea) or networkRef.element.oclIsKindOf(RunwayArea)". Verify that a [ConditionOfAirFacility](#ConditionOfAirFacility) is only associated with a spatial object [AerodromeNode](#AerodromeNode), [AerodromeArea](#AerodromeArea) or [RunwayArea](#RunwayArea).
* ElementLength can only be associated with a spatial object that is a Runway Area, Taxiway Area or Touch Down Lift Off; OCL: "inv: networkRef.element.oclIsKindOf(RunwayArea) or networkRef.element.oclIsKindOf(TaxiwayArea) or networkRef.element.oclIsKindOf(TouchDownLiftOff)." Verify that an [ElementLength](#ElementLength) is only associated with a spatial object [RunwayArea](#RunwayArea), [TaxiwayArea](#TaxiwayArea) or [TouchDownLiftOff](#TouchDownLiftOff).
* ElementWidth can only be associated with a spatial object that is a Runway Area, Taxiway Area or Touch Down Lift Off; OCL: "inv: networkRef.element.oclIsKindOf(RunwayArea) or networkRef.element.oclIsKindOf(TaxiwayArea) or networkRef.element.oclIsKindOf(TouchDownLiftOff)". Verify that an [ElementWidth](#ElementWidth) is only associated with a spatial object [RunwayArea](#RunwayArea), [TaxiwayArea](#TaxiwayArea) or [TouchDownLiftOff](#TouchDownLiftOff).
* FieldElevation can only be associated with a spatial object that is an Aerodrome Node or Aerodrome Area; OCL: "inv: networkRef.element.oclIsKindOf(AerodromeNode) or networkRef.element.oclIsKindOf(AerodromeArea)". Verify that a [FieldElevation](#FieldElevation) is only associated with a spatial object [AerodromeNode](#AerodromeNode) or [AerodromeArea](#AerodromeArea).
* LowerAltitudeLimit can only be associated with a spatial object that is an Air Route Link or Airspace Area; OCL: "inv: networkRef.element.oclIsKindOf(AirRouteLink) or networkRef.element.oclIsKindOf(AirspaceArea)". Verify that a [LowerAltitudeLimit](#LowerAltitudeLimit) is only associated with a spatial object [AirRouteLink](#AirRouteLink) or [AirspaceArea](#AirspaceArea).
* SurfaceComposition can only be associated with a spatial object that is a Runway Area, Taxiway Area, Apron Area or Touch Down Lift Off; OCL: "inv: networkRef.element.oclIsKindOf(RunwayArea) or networkRef.element.oclIsKindOf(TaxiwayArea) or networkRef.element.oclIsKindOf(ApronArea) or networkRef.element.oclIsKindOf(TouchDownLiftOff)". Verify that a [SurfaceComposition](#SurfaceComposition) is only associated with a spatial object [RunwayArea](#RunwayArea), [TaxiwayArea](#TaxiwayArea), [ApronArea](#ApronArea) or [TouchDownLiftOff](#TouchDownLiftOff).
* UpperAltitudeLimit can only be associated with a spatial object that is an Air Route Link or Airspace Area; OCL: "inv: networkRef.element.oclIsKindOf(AirRouteLink) or networkRef.element.oclIsKindOf(AirspaceArea)". Verify that an [UpperAltitudeLimit](#UpperAltitudeLimit) is only associated with a spatial object [AirRouteLink](#AirRouteLink) or [AirspaceArea](#AirspaceArea).
* UseRestriction can only be associated with a spatial object that is an Air Route, Air Link (or specialized Air Link), Air Node (or specialized Air Node) or Aerodrome Area; OCL: "inv: networkRef.element.oclIsKindOf(AirRoute) or networkRef.element.oclIsKindOf(AirLink) or networkRef.element.oclIsKindOf(AirNode) or networkRef.element.oclIsKindOf(AerodromeArea)". Verify that a [UseRestriction](#UseRestriction) is only associated with a spatial object [AirRoute](#AirRoute), [AirLink](#AirLink), [AirNode](#AirNode) or [AerodromeArea](#AerodromeArea).

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-ad/3.2/ad-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-AD](http://inspire.ec.europa.eu/id/ats/data-ad/3.2/ad-as/README#ref_TG_DS_AD)) 5.4

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-p-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
AerodromeCategory <a name="AerodromeCategory"></a> 	| 	//schema-element(
AerodromeNode <a name="AerodromeNode"></a>   | //schema-element(
AerodromeArea <a name="AerodromeArea"></a>  | //schema-element(
AerodromeType <a name="AerodromeType"></a> 	| 	//schema-element(
ConditionOfAirFacility <a name="ConditionOfAirFacility"></a> 	| 	//schema-element(
RunwayArea <a name="RunwayArea"></a> 	| 	//schema-element(
ElementLength <a name="ElementLength"></a> 	| 	//schema-element(
ElementWidth <a name="ElementWidth"></a> 	| 	//schema-element(
TaxiwayArea <a name="TaxiwayArea"></a> 	| 	//schema-element(
TouchDownLiftOff <a name="TouchDownLiftOff"></a> 	| 	//schema-element(
FieldElevation <a name="FieldElevation"></a> 	| 	//schema-element(
LowerAltitudeLimit <a name="LowerAltitudeLimit"></a> 	| 	//schema-element(
UpperAltitudeLimit <a name="UpperAltitudeLimit"></a> 	| 	//schema-element(
AirRouteLink <a name="AirRouteLink"></a> 	| 	//schema-element(
AirRoute <a name="AirRoute"></a> 	| 	//schema-element(
AirLink <a name="AirLink"></a> 	| 	//schema-element(
AirNode <a name="AirNode"></a> 	| 	//schema-element(
AirspaceArea <a name="AirspaceArea"></a> 	| 	//schema-element(
SurfaceComposition <a name="SurfaceComposition"></a> 	| 	//schema-element(
ApronArea <a name="ApronArea"></a> 	| 	//schema-element(
UseRestriction <a name="UseRestriction"></a> 	| 	//schema-element(
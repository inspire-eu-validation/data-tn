# Code list values

**Version**: 1

**Purpose**: Verify whether all attributes whose value type is a code list take the values set out therein

**Prerequisites**

**Test method**

When an attribute has a code list as its type, verify that the values comply with the definitions and include the values set out in Annex II of the regulation. To pass this tests that any instance of an attribute

* takes only values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'none'.

Otherwise report [disallowedCodeListValue](#disallowedCodeListValue).

In the Addresses application schema, the following properties have to be tested:
* [FormOfRailwayNodeValue (v3)](#FormOfRailwayNodeValue3). Valid values:
  * junction
  * levelCrossing
  * pseudoNode
  * railwayEnd
  * railwayStop
* [FormOfRailwayNodeValue (v4)](#FormOfRailwayNodeValue4). Valid values:
  * http://inspire.ec.europa.eu/codelist/FormOfRailwayNodeValue/junction
  * http://inspire.ec.europa.eu/codelist/FormOfRailwayNodeValue/levelCrossing
  * http://inspire.ec.europa.eu/codelist/FormOfRailwayNodeValue/pseudoNode
  * http://inspire.ec.europa.eu/codelist/FormOfRailwayNodeValue/railwayEnd
  * http://inspire.ec.europa.eu/codelist/FormOfRailwayNodeValue/railwayStop
* [RailwayTypeValue (v3)](#RailwayTypeValue3). Valid values:
  * cogRailway
  * funicular
  * magneticLevitation
  * metro
  * monorail
  * suspendedRail
  * train
  * tramway
* [RailwayTypeValue (v4)](#RailwayTypeValue4). Valid values:
  * http://inspire.ec.europa.eu/codelist/RailwayTypeValue/cogRailway
  * http://inspire.ec.europa.eu/codelist/RailwayTypeValue/funicular
  * http://inspire.ec.europa.eu/codelist/RailwayTypeValue/magneticLevitation
  * http://inspire.ec.europa.eu/codelist/RailwayTypeValue/metro
  * http://inspire.ec.europa.eu/codelist/RailwayTypeValue/monorail
  * http://inspire.ec.europa.eu/codelist/RailwayTypeValue/suspendedRail
  * http://inspire.ec.europa.eu/codelist/RailwayTypeValue/train
  * http://inspire.ec.europa.eu/codelist/RailwayTypeValue/tramway
* [RailwayUseValue (v3)](#RailwayUseValue3). Valid values:
  * cargo
  * carShuttle
  * mixed
  * passengers
* [RailwayUseValue (v4)](#RailwayUseValue4). Valid values:
  * http://inspire.ec.europa.eu/codelist/RailwayUseValue/carShuttle
  * http://inspire.ec.europa.eu/codelist/RailwayUseValue/cargo
  * http://inspire.ec.europa.eu/codelist/RailwayUseValue/mixed
  * http://inspire.ec.europa.eu/codelist/RailwayUseValue/passengers

The following is not applicable for this application schema as no extensions are allowed. It is still included here as a reminder in case extensions will be allowed in the future:

Inspect the code list valued property elements. If a value is not one of the values listed above, review the code list definition to check that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule and that all extensions conform to the requirements. This is a manual test.
  
**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ra-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ra-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (3)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ra-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ra-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (2)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ra-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (3)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ra-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (4)

**Test type**: Automated

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
disallowedCodeListValue <a name="disallowedCodeListValue"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that is not one of the allowed values listed at $codelist. 

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ra-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
AerodromeCategoryValue (v3) <a name="AerodromeCategoryValue3"></a>  | //schema-element(tn-a3:AerodromeCategory/tn-a3:aerodromeCategory/text()
AerodromeCategoryValue (v4) <a name="AerodromeCategoryValue4"></a>  | //schema-element(tn-a:AerodromeCategory/tn-a:aerodromeCategory/@href:xlink
AerodromeTypeValue (v3) <a name="AerodromeTypeValue3"></a>          | //schema-element(tn-a3:AerodromeType/tn-a3:aerodromeType/text()
AerodromeTypeValue (v4) <a name="AerodromeTypeValue4"></a>          | //schema-element(tn-a:AerodromeType/tn-a:aerodromeType/@href:xlink
AirRouteLinkClassValue (v3) <a name="AirRouteLinkClassValue3"></a>  | //schema-element(tn-a3:AirRouteLink/tn-a3:airRouteLinkClass/text()
AirRouteLinkClassValue (v4) <a name="AirRouteLinkClassValue4"></a>  | //schema-element(tn-a:AirRouteLink/tn-a:airRouteLinkClass/@href:xlink
AirRouteTypeValue (v3) <a name="AirRouteTypeValue3"></a>            | //schema-element(tn-a3:AirRoute/tn-a3:airRouteType/text()
AirRouteTypeValue (v4) <a name="AirRouteTypeValue4"></a>            | //schema-element(tn-a:AirRoute/tn-a:airRouteType/@href:xlink
AirUseRestrictionValue (v3) <a name="AirUseRestrictionValue3"></a>  | //schema-element(tn-a3:useRestriction/tn-a3:restriction/text()
AirUseRestrictionValue (v4) <a name="AirUseRestrictionValue4"></a>  | //schema-element(tn-a:useRestriction/tn-a:restriction/@href:xlink
AirspaceAreaTypeValue (v3) <a name="AirspaceAreaTypeValue3"></a>    | //schema-element(tn-a3:AirspaceArea/tn-a3:AirspaceAreaType/text()
AirspaceAreaTypeValue (v4) <a name="AirspaceAreaTypeValue4"></a>    | //schema-element(tn-a:AirspaceArea/tn-a:AirspaceAreaType/@href:xlink
NavaidTypeValue (v3) <a name="NavaidTypeValue3"></a>                | //schema-element(tn-a3:Navaid/tn-a3:navaidType/text()
NavaidTypeValue (v4) <a name="NavaidTypeValue4"></a>                | //schema-element(tn-a:Navaid/tn-a:navaidType/@href:xlink
PointRoleValue (v3) <a name="PointRoleValue3"></a>                  | //schema-element(tn-a3:RunwayCentrelinePoint/tn-a3:pointRole/text()
PointRoleValue (v4) <a name="PointRoleValue4"></a>                  | //schema-element(tn-a:RunwayCentrelinePoint/tn-a:pointRole/@href:xlink
RunwayTypeValue (v3) <a name="RunwayTypeValue3"></a>                | //schema-element(tn-a3:RunwayArea/tn-a3:runwayType/text()
RunwayTypeValue (v4) <a name="RunwayTypeValue4"></a>                | //schema-element(tn-a:RunwayArea/tn-a:runwayType/@href:xlink
SurfaceCompositionValue (v3) <a name="SurfaceCompositionValue3"></a>| //schema-element(tn-a3:SurfaceComposition/tn-a3:surfaceComposition/text()
SurfaceCompositionValue (v4) <a name="SurfaceCompositionValue4"></a>| //schema-element(tn-a:SurfaceComposition/tn-a:surfaceComposition/@href:xlink
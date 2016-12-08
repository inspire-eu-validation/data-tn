# Code list values

**Version**: 1

**Purpose**: Verify whether all attributes whose value type is a code list take the values set out therein

**Prerequisites**

**Test method**

When an attribute has a code list as its type, verify that the values comply with the definitions and include the values set out in Annex II of the regulation. To pass this tests that any instance of an attribute

* takes only values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'none'.

Otherwise report [disallowedCodeListValue](#disallowedCodeListValue).

In the Addresses application schema, the following properties have to be tested:
* [FerryUseValue (v3)](#FerryUseValue3). Valid values:
  * cars
  * other
  * passengers
  * train
  * trucks
* [FerryUseValue (v4)](#FerryUseValue4). Valid values:
  * http://inspire.ec.europa.eu/codelist/FerryUseValue/cars
  * http://inspire.ec.europa.eu/codelist/FerryUseValue/other
  * http://inspire.ec.europa.eu/codelist/FerryUseValue/passengers
  * http://inspire.ec.europa.eu/codelist/FerryUseValue/trains
  * http://inspire.ec.europa.eu/codelist/FerryUseValue/trucks
* [FormOfWaterwayNodeValue (v3)](#FormOfWaterwayNodeValue3). Valid values:
  * junctionFork
  * lockComplex
  * movableBridge
  * shipLift
  * turningBasin
  * waterTerminal
* [FormOfWaterwayNodeValue (v4)](#FormOfWaterwayNodeValue4). Valid values:
  * http://inspire.ec.europa.eu/codelist/FormOfWaterwayNodeValue/junctionFork
  * http://inspire.ec.europa.eu/codelist/FormOfWaterwayNodeValue/lockComplex
  * http://inspire.ec.europa.eu/codelist/FormOfWaterwayNodeValue/movableBridge
  * http://inspire.ec.europa.eu/codelist/FormOfWaterwayNodeValue/shipLift
  * http://inspire.ec.europa.eu/codelist/FormOfWaterwayNodeValue/turningBasin
  * http://inspire.ec.europa.eu/codelist/FormOfWaterwayNodeValue/waterTerminal


The following is not applicable for this application schema as no extensions are allowed. It is still included here as a reminder in case extensions will be allowed in the future:

Inspect the code list valued property elements. If a value is not one of the values listed above, review the code list definition to check that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule and that all extensions conform to the requirements. This is a manual test.
  
**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-w-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-w-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (3)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-w-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-w-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (2)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-w-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (3)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-w-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (4)

**Test type**: Automated

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
disallowedCodeListValue <a name="disallowedCodeListValue"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that is not one of the allowed values listed at $codelist. 

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-w-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
FerryUseValue (v3) <a name="FerryUseValue3"></a>                      | //schema-element(tn-w3:FerryUse)/tn-w3:ferryUse/text()
FerryUseValue (v4) <a name="FerryUseValue4"></a>                      | //schema-element(tn-w:FerryUse)/tn-w:ferryUse/@href:xlink
FormOfWaterwayNodeValue (v3) <a name="FormOfWaterwayNodeValue3"></a>  | //schema-element(tn-w3:WaterwayNode)/tn-w3:formOfWaterwayNode/text()
FormOfWaterwayNodeValue (v4) <a name="FormOfWaterwayNodeValue4"></a>  | //schema-element(tn-w:WaterwayNode)/tn-w:formOfWaterwayNode/@href:xlink
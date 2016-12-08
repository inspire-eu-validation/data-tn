# Conformance class: Application schema, Rail Transport Networks (DRAFT)

Conformance class for the requirements associated with the application schema. 

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schema for Rail Transport Networks".

This conformance class is part of the [Abstract Test Suite for the INSPIRE Data Specification on Transport Networks](http://inspire.ec.europa.eu/id/ats/data-tn/3.2).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

none

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-TN](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ra-as/README#ref_TG_DS_TN) | [GML application schema, Rail Transport Networks](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-gml) | INSPIRE spatial data set encoded in GML, Rail Transport Networks features | n/a |
| [TG DS-TN](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ra-as/README#ref_TG_DS_TN) | [Application schema, Transport Networks](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-as) | INSPIRE spatial data set, Transport Networks features | n/a |
 
## Feature types <a name="feature-types"></a>

The instantiable feature types in the application schema are:

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

*Note*: When "features" or "spatial objects" are mentioned in the test cases, this refers only to instances of feature types of this application schema, not to any types specified in any other application schema.

## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
TG DS-TN <a name="ref_TG_DS_TN"></a>   | [INSPIRE Data Specification on Transport Networks – Technical Guidelines version 3.2](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_TN_v3.2.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-TN](#ref_TG_DS_TN)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Code list values](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ra-as/code-list-values)  | Draft  | A.1.3, A.6.1  |
| [Constraints](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ra-as/constraints)  | Draft  | A.1.6  |


## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
tn-ra3			| urn:x-inspire:specification:gmlas:RailwayTransportNetwork:3.0
tn-ra			| http://inspire.ec.europa.eu/schemas/tn-ra/4.0
base           | http://inspire.ec.europa.eu/schemas/base/3.3
gml            | http://www.opengis.net/gml/3.2
wfs            | http://www.opengis.net/wfs/2.0
xsi            | http://www.w3.org/2001/XMLSchema-instance
xlink          | http://www.w3.org/1999/xlink
xml            | http://www.w3.org/XML/1998/namespace

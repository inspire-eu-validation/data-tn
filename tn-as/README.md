# Conformance class: Application schema, Transport Networks Common (DRAFT)

Conformance class for the requirements associated with the application schema. 

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schema for Transport Networks".

This conformance class is part of the [Abstract Test Suite for the INSPIRE Data Specification on Transport Networks](http://inspire.ec.europa.eu/id/ats/data-tn/3.2).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

none

Note that there is a dependency on the requirements related to the Generic Network Model application schema. This application schema only adds two requirements (two OCL constraints) that are not already covered by the tests for the conformance class "INSPIRE GML application schemas". As the tests for the Transport Network application schemas include more specific constraints, it is not necessary to create a separate Abstract Test Suite for the Generic Network Model application schema. 

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-TN](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-as/README#ref_TG_DS_TN) | [GML application schema, Transport Networks](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-gml) | INSPIRE spatial data set encoded in GML, Transport Networks features | n/a |
 
## Feature types <a name="feature-types"></a>

The instantiable feature types in the application schema are:

* AccessRestriction
* ConditionOfFacility
* MaintenanceAuthority
* MarkerPost
* OwnerAuthority
* RestrictionForVehicles
* TrafficFlowDirection
* TransportNetwork
* VerticalPosition

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
| [Code list values](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-as/code-list-values)  | Draft  | A.1.3, A.6.1  |
| [Constraints](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-as/constraints)  | Draft  | A.1.6  |
| [Geometry](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-as/geometry)  | Draft  | A.1.7  |
| [Object Reference Modelling](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-as/object-references)  | Draft  | A.1.8  |
| [Network Connectivity](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-as/network-connectivity)  | Draft  | A.1.10  |


## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
tn3            	| urn:x-inspire:specification:gmlas:CommonTransportElements:3.0
tn           	| http://inspire.ec.europa.eu/schemas/tn/4.0
base           | http://inspire.ec.europa.eu/schemas/base/3.3
gml            | http://www.opengis.net/gml/3.2
wfs            | http://www.opengis.net/wfs/2.0
xsi            | http://www.w3.org/2001/XMLSchema-instance
xlink          | http://www.w3.org/1999/xlink
xml            | http://www.w3.org/XML/1998/namespace

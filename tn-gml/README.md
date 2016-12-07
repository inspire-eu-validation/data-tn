# Conformance class: GML application schema, Transport Networks Simple (DRAFT)

Conformance class for the GML encoding of spatial objects specified in the INSPIRE GML application schema 'Transport Networks Simple'. This conformance class examines the data set against requirements associated with the GML application schema. Both currently approved GML application schema versions (3.0 and 4.0) are tested.

This conformance class is part of the [Abstract Test Suite for the INSPIRE Data Specification on Transport Networks](http://inspire.ec.europa.eu/id/ats/data-tn/3.2).

## Standardization target type

INSPIRE spatial data set encoded in GML, Transport Networks features

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the GML documents, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [TG DS Template](#ref_TG_DS_tmpl) | [INSPIRE GML application schemas](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/schemas) | n/a |

### Indirect dependencies

n/a
 
## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
TG DS-TN <a name="ref_TG_DS_TN"></a>   | [INSPIRE Data Specification on Transport Networks – Technical Guidelines version 3.2](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_TN_v3.2.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-TN](#ref_TG_DS_TN)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Basic test](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-gml/basic)  | ready for review  | A.1.1, (A.6.1)  |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
tn3            	| urn:x-inspire:specification:gmlas:CommonTransportElements:3.0
tn           	| http://inspire.ec.europa.eu/schemas/tn/4.0
tn-ro3			| urn:x-inspire:specification:gmlas:RoadTransportNetwork:3.0
tn-ro			| http://inspire.ec.europa.eu/schemas/tn-ro/4.0
tn-ra3			| urn:x-inspire:specification:gmlas:RailwayTransportNetwork:3.0
tn-ra			| http://inspire.ec.europa.eu/schemas/tn-ra/4.0
tn-c3			| urn:x-inspire:specification:gmlas:CableTransportNetwork:3.0
tn-c			| http://inspire.ec.europa.eu/schemas/tn-c/4.0
tn-w3			| urn:x-inspire:specification:gmlas:WaterTransportNetwork:3.0
tn-w			| http://inspire.ec.europa.eu/schemas/tn-w/4.0
tn-a3			| urn:x-inspire:specification:gmlas:AirTransportNetwork:3.0
tn-a			| http://inspire.ec.europa.eu/schemas/tn-a/4.0
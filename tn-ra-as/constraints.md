# Constraints

**Version**: 1

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

Verify that the OCL constraints listed below that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation). 

For constraints that require retrieving a referenced resource and the resource cannot be retrieved, report [brokenLink](#brokenLink). The test accepts the following two types of content in @xlink:href attributes: Either a "#" followed by a @gml:id in the same document or a HTTP URI.

Automated tests:

* DesignSpeed can only be associated with a spatial object that is part of a railway transport network; OCL: "inv: networkRef.element.oclIsKindOf(RailwayArea) or networkRef.element.oclIsKindOf(RailwayYardArea) or networkRef.element.oclIsKindOf(RailwayStationArea) or networkRef.element.oclIsKindOf(RailwayLine) or networkRef.element.oclIsKindOf(RailwayLinkSequence) or networkRef.element.oclIsKindOf(RailwayLink) or networkRef.element.oclIsKindOf(RailwayNode)". Verify that a [DesignSpeed](#DesignSpeed) is only associated with a spatial object [RailwayArea](#RailwayArea), [RailwayYardArea](#RailwayYardArea), [RailwayStationArea](#RailwayStationArea), [RailwayLine](#RailwayLine), [RailwayLinkSequence](#RailwayLinkSequence), [RailwayLink](#RailwayLink),  or [RailwayNode](#RailwayNode).
* NominalTrackGauge can only be associated with a spatial object that is part of a railway transport network; OCL: "inv: networkRef.element.oclIsKindOf(RailwayArea) or networkRef.element.oclIsKindOf(RailwayYardArea) or networkRef.element.oclIsKindOf(RailwayStationArea) or networkRef.element.oclIsKindOf(RailwayLine) or networkRef.element.oclIsKindOf(RailwayLinkSequence) or networkRef.element.oclIsKindOf(RailwayLink) or networkRef.element.oclIsKindOf(RailwayNode)". Verify that a [NominalTrackGauge](#NominalTrackGauge) is only associated with a spatial object [RailwayArea](#RailwayArea), [RailwayYardArea](#RailwayYardArea), [RailwayStationArea](#RailwayStationArea), [RailwayLine](#RailwayLine), [RailwayLinkSequence](#RailwayLinkSequence), [RailwayLink](#RailwayLink),  or [RailwayNode](#RailwayNode).
* NumberOfTracks can only be associated with a spatial object that is part of a railway transport network; OCL: "inv: networkRef.element.oclIsKindOf(RailwayArea) or networkRef.element.oclIsKindOf(RailwayYardArea) or networkRef.element.oclIsKindOf(RailwayStationArea) or networkRef.element.oclIsKindOf(RailwayLine) or networkRef.element.oclIsKindOf(RailwayLinkSequence) or networkRef.element.oclIsKindOf(RailwayLink) or networkRef.element.oclIsKindOf(RailwayNode)". Verify that a [NumberOfTracks](#NumberOfTracks) is only associated with a spatial object [RailwayArea](#RailwayArea), [RailwayYardArea](#RailwayYardArea), [RailwayStationArea](#RailwayStationArea), [RailwayLine](#RailwayLine), [RailwayLinkSequence](#RailwayLinkSequence), [RailwayLink](#RailwayLink),  or [RailwayNode](#RailwayNode).
* RailwayElectrification can only be associated with a spatial object that is part of a railway transport network; OCL: "inv: networkRef.element.oclIsKindOf(RailwayArea) or networkRef.element.oclIsKindOf(RailwayYardArea) or networkRef.element.oclIsKindOf(RailwayStationArea) or networkRef.element.oclIsKindOf(RailwayLine) or networkRef.element.oclIsKindOf(RailwayLinkSequence) or networkRef.element.oclIsKindOf(RailwayLink) or networkRef.element.oclIsKindOf(RailwayNode)". Verify that a [RailwayElectrification](#RailwayElectrification) is only associated with a spatial object [RailwayArea](#RailwayArea), [RailwayYardArea](#RailwayYardArea), [RailwayStationArea](#RailwayStationArea), [RailwayLine](#RailwayLine), [RailwayLinkSequence](#RailwayLinkSequence), [RailwayLink](#RailwayLink),  or [RailwayNode](#RailwayNode).
* RailwayStationCode can only be associated with a spatial object that is part of a railway transport network; OCL: "inv: networkRef.element.oclIsKindOf(RailwayArea) or networkRef.element.oclIsKindOf(RailwayYardArea) or networkRef.element.oclIsKindOf(RailwayStationArea) or networkRef.element.oclIsKindOf(RailwayLine) or networkRef.element.oclIsKindOf(RailwayLinkSequence) or networkRef.element.oclIsKindOf(RailwayLink) or networkRef.element.oclIsKindOf(RailwayNode)". Verify that a [RailwayStationCode](#RailwayStationCode) is only associated with a spatial object [RailwayArea](#RailwayArea), [RailwayYardArea](#RailwayYardArea), [RailwayStationArea](#RailwayStationArea), [RailwayLine](#RailwayLine), [RailwayLinkSequence](#RailwayLinkSequence), [RailwayLink](#RailwayLink),  or [RailwayNode](#RailwayNode).
* RailwayType can only be associated with a spatial object that is part of a railway transport network; OCL: "inv: networkRef.element.oclIsKindOf(RailwayArea) or networkRef.element.oclIsKindOf(RailwayYardArea) or networkRef.element.oclIsKindOf(RailwayStationArea) or networkRef.element.oclIsKindOf(RailwayLine) or networkRef.element.oclIsKindOf(RailwayLinkSequence) or networkRef.element.oclIsKindOf(RailwayLink) or networkRef.element.oclIsKindOf(RailwayNode)". Verify that a [RailwayType](#RailwayType) is only associated with a spatial object [RailwayArea](#RailwayArea), [RailwayYardArea](#RailwayYardArea), [RailwayStationArea](#RailwayStationArea), [RailwayLine](#RailwayLine), [RailwayLinkSequence](#RailwayLinkSequence), [RailwayLink](#RailwayLink),  or [RailwayNode](#RailwayNode).
* RailwayUse can only be associated with a spatial object that is part of a railway transport network; OCL: "inv: networkRef.element.oclIsKindOf(RailwayArea) or networkRef.element.oclIsKindOf(RailwayYardArea) or networkRef.element.oclIsKindOf(RailwayStationArea) or networkRef.element.oclIsKindOf(RailwayLine) or networkRef.element.oclIsKindOf(RailwayLinkSequence) or networkRef.element.oclIsKindOf(RailwayLink) or networkRef.element.oclIsKindOf(RailwayNode)". Verify that a [RailwayUse](#RailwayUse) is only associated with a spatial object [RailwayArea](#RailwayArea), [RailwayYardArea](#RailwayYardArea), [RailwayStationArea](#RailwayStationArea), [RailwayLine](#RailwayLine), [RailwayLinkSequence](#RailwayLinkSequence), [RailwayLink](#RailwayLink),  or [RailwayNode](#RailwayNode).
* For a railway station node, the value for the "formOfNode" attribute shall always be "RailwayStop"; OCL:"formOfNode = FormOfRailwayNodeValue::railwayStop". Verify that the value of the attribute [formOfNode](#formOfNode) of all [RailwayStationNode](#RailwayStationNode) is RailwayStop.
* For a railway yard node, the value for the "formOfNode" attribute shall always be "RailwayStop"; OCL: "formOfNode = FormOfRailwayNodeValue::railwayStop". Verify that the value of the attribute [formOfNode](#formOfNode) of all [RailwayYardNode](#RailwayYardNode) is RailwayStop.



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
DesignSpeed <a name="DesignSpeed"></a> 					| 	//schema-element( 
NominalTrackGauge <a name="NominalTrackGauge"></a> 		| 	//schema-element( 
NumberOfTracks <a name="NumberOfTracks"></a> 			| 	//schema-element( 
RailwayElectrification <a name="RailwayElectrification"></a> | //schema-element( 
RailwayStationCode <a name="RailwayStationCode"></a> 	| 	//schema-element( 
RailwayType <a name="RailwayType"></a> 					| 	//schema-element( 
RailwayUse <a name="RailwayUse"></a> 					| 	//schema-element( 
RailwayArea <a name="RailwayArea"></a> 					| 	//schema-element(
RailwayYardArea <a name="RailwayYardArea"></a> 			| 	//schema-element(
RailwayStationArea <a name="RailwayStationArea"></a> 	| 	//schema-element(
RailwayLine <a name="RailwayLine"></a> 					| 	//schema-element(
RailwayLinkSequence <a name="RailwayLinkSequence"></a> 	| 	//schema-element(
RailwayLink <a name="RailwayLink"></a> 					| 	//schema-element(
RailwayNode <a name="RailwayNode"></a> 					| 	//schema-element(
formOfNode <a name="formOfNode"></a> 					| 	//schema-element( 
RailwayStationNode <a name="RailwayStationNode"></a> 	| 	//schema-element(
RailwayYardNode <a name="RailwayYardNode"></a> 			| 	//schema-element(
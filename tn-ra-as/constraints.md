# Constraints

**Version**: 1

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

Verify that the OCL constraints listed below that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation). 

For constraints that require retrieving a referenced resource and the resource cannot be retrieved, report [brokenLink](#brokenLink). The test accepts the following two types of content in @xlink:href attributes: Either a "#" followed by a @gml:id in the same document or a HTTP URI.

Automated tests:

* DesignSpeed can only be associated with a spatial object that is part of a railway transport network; OCL: "inv: networkRef.element.oclIsKindOf(RailwayArea) or networkRef.element.oclIsKindOf(RailwayYardArea) or networkRef.element.oclIsKindOf(RailwayStationArea) or networkRef.element.oclIsKindOf(RailwayLine) or networkRef.element.oclIsKindOf(RailwayLinkSequence) or networkRef.element.oclIsKindOf(RailwayLink) or networkRef.element.oclIsKindOf(RailwayNode)". Verify that a [DesignSpeed](#DesignSpeed) only has a [Network element association](#NetworkElement1) with a spatial object RailwayArea, RailwayYardArea, RailwayStationArea, RailwayLine, RailwayLinkSequence, RailwayLink,  or RailwayNode.
* NominalTrackGauge can only be associated with a spatial object that is part of a railway transport network; OCL: "inv: networkRef.element.oclIsKindOf(RailwayArea) or networkRef.element.oclIsKindOf(RailwayYardArea) or networkRef.element.oclIsKindOf(RailwayStationArea) or networkRef.element.oclIsKindOf(RailwayLine) or networkRef.element.oclIsKindOf(RailwayLinkSequence) or networkRef.element.oclIsKindOf(RailwayLink) or networkRef.element.oclIsKindOf(RailwayNode)". Verify that a [NominalTrackGauge](#NominalTrackGauge) only has a [Network element association](#NetworkElement2) with a spatial object RailwayArea, RailwayYardArea, RailwayStationArea, RailwayLine, RailwayLinkSequence, RailwayLink,  or RailwayNode.
* NumberOfTracks can only be associated with a spatial object that is part of a railway transport network; OCL: "inv: networkRef.element.oclIsKindOf(RailwayArea) or networkRef.element.oclIsKindOf(RailwayYardArea) or networkRef.element.oclIsKindOf(RailwayStationArea) or networkRef.element.oclIsKindOf(RailwayLine) or networkRef.element.oclIsKindOf(RailwayLinkSequence) or networkRef.element.oclIsKindOf(RailwayLink) or networkRef.element.oclIsKindOf(RailwayNode)". Verify that a [NumberOfTracks](#NumberOfTracks) only has a [Network element association](#NetworkElement3) with a spatial object RailwayArea, RailwayYardArea, RailwayStationArea, RailwayLine, RailwayLinkSequence, RailwayLink,  or RailwayNode.
* RailwayElectrification can only be associated with a spatial object that is part of a railway transport network; OCL: "inv: networkRef.element.oclIsKindOf(RailwayArea) or networkRef.element.oclIsKindOf(RailwayYardArea) or networkRef.element.oclIsKindOf(RailwayStationArea) or networkRef.element.oclIsKindOf(RailwayLine) or networkRef.element.oclIsKindOf(RailwayLinkSequence) or networkRef.element.oclIsKindOf(RailwayLink) or networkRef.element.oclIsKindOf(RailwayNode)". Verify that a [RailwayElectrification](#RailwayElectrification) only has a [Network element association](#NetworkElement4) with a spatial object RailwayArea, RailwayYardArea, RailwayStationArea, RailwayLine, RailwayLinkSequence, RailwayLink,  or RailwayNode.
* RailwayStationCode can only be associated with a spatial object that is part of a railway transport network; OCL: "inv: networkRef.element.oclIsKindOf(RailwayArea) or networkRef.element.oclIsKindOf(RailwayYardArea) or networkRef.element.oclIsKindOf(RailwayStationArea) or networkRef.element.oclIsKindOf(RailwayLine) or networkRef.element.oclIsKindOf(RailwayLinkSequence) or networkRef.element.oclIsKindOf(RailwayLink) or networkRef.element.oclIsKindOf(RailwayNode)". Verify that a [RailwayStationCode](#RailwayStationCode) only has a [Network element association](#NetworkElement5) with a spatial object RailwayArea, RailwayYardArea, RailwayStationArea, RailwayLine, RailwayLinkSequence, RailwayLink,  or RailwayNode.
* RailwayType can only be associated with a spatial object that is part of a railway transport network; OCL: "inv: networkRef.element.oclIsKindOf(RailwayArea) or networkRef.element.oclIsKindOf(RailwayYardArea) or networkRef.element.oclIsKindOf(RailwayStationArea) or networkRef.element.oclIsKindOf(RailwayLine) or networkRef.element.oclIsKindOf(RailwayLinkSequence) or networkRef.element.oclIsKindOf(RailwayLink) or networkRef.element.oclIsKindOf(RailwayNode)". Verify that a [RailwayType](#RailwayType) only has a [Network element association](#NetworkElement6) with a spatial object RailwayArea, RailwayYardArea, RailwayStationArea, RailwayLine, RailwayLinkSequence, RailwayLink,  or RailwayNode.
* RailwayUse can only be associated with a spatial object that is part of a railway transport network; OCL: "inv: networkRef.element.oclIsKindOf(RailwayArea) or networkRef.element.oclIsKindOf(RailwayYardArea) or networkRef.element.oclIsKindOf(RailwayStationArea) or networkRef.element.oclIsKindOf(RailwayLine) or networkRef.element.oclIsKindOf(RailwayLinkSequence) or networkRef.element.oclIsKindOf(RailwayLink) or networkRef.element.oclIsKindOf(RailwayNode)". Verify that a [RailwayUse](#RailwayUse) only has a [Network element association](#NetworkElement7) with a spatial object RailwayArea, RailwayYardArea, RailwayStationArea, RailwayLine, RailwayLinkSequence, RailwayLink,  or RailwayNode.
* For a railway station node, the value for the "formOfNode" attribute shall always be "RailwayStop"; OCL:"formOfNode = FormOfRailwayNodeValue::railwayStop". Verify that the value of the attribute [formOfNode](#formOfNode1) of all [RailwayStationNode](#RailwayStationNode) is RailwayStop.
* For a railway yard node, the value for the "formOfNode" attribute shall always be "RailwayStop"; OCL: "formOfNode = FormOfRailwayNodeValue::railwayStop". Verify that the value of the attribute [formOfNode](#formOfNode2) of all [RailwayYardNode](#RailwayYardNode) is RailwayStop.

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ra-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-TN](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ra-as/README#ref_TG_DS_TN)) 5.4

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-tn/3.2/tn-ra-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
DesignSpeed <a name="DesignSpeed"></a> 											| //schema-element(tn-ra:DesignSpeed)
Network element association DesignSpeed <a name="NetworkElement1"></a>  		| //schema-element(tn-ra:DesignSpeed)/net:networkRef/*/net:element/@xlink:href 
NominalTrackGauge <a name="NominalTrackGauge"></a> 								| //schema-element(tn-ra:NominalTrackGauge)
Network element association NominalTrackGauge <a name="NetworkElement2"></a>   	| //schema-element(tn-ra:NominalTrackGauge)/net:networkRef/*/net:element/@xlink:href 
NumberOfTracks <a name="NumberOfTracks"></a> 									| //schema-element(tn-ra:NumberOfTracks)
Network element association NumberOfTracks <a name="NetworkElement3"></a>   	| //schema-element(tn-ra:NumberOfTracks)/net:networkRef/*/net:element/@xlink:href 
RailwayElectrification <a name="RailwayElectrification"></a> 					| //schema-element(tn-ra:RailwayElectrification)
Network element association RailwayElectrification <a name="NetworkElement4"></a> | //schema-element(tn-ra:RailwayElectrification)/net:networkRef/*/net:element/@xlink:href 
RailwayStationCode <a name="RailwayStationCode"></a> 							| //schema-element(tn-ra:RailwayStationCode)
Network element association RailwayStationCode <a name="NetworkElement5"></a>  	| //schema-element(tn-ra:RailwayStationCode)/net:networkRef/*/net:element/@xlink:href 
RailwayType <a name="RailwayType"></a> 											| //schema-element(tn-ra:RailwayType)
Network element association RailwayType <a name="NetworkElement6"></a>   		| //schema-element(tn-ra:RailwayType)/net:networkRef/*/net:element/@xlink:href 
RailwayUse <a name="RailwayUse"></a> 											| //schema-element(tn-ra:RailwayUse)
Network element association RailwayUse <a name="NetworkElement7"></a>   		| //schema-element(tn-ra:RailwayUse)/net:networkRef/*/net:element/@xlink:href 
formOfNode attribute for RailwayStationNode <a name="formOfNode1"></a> 			| //schema-element(tn-ra:RailwayStationNode)/formOfNode
formOfNode attribute for RailwayYardNode <a name="formOfNode2"></a> 			| //schema-element(tn-ra:RailwayYardNode)/formOfNode
RailwayStationNode <a name="RailwayStationNode"></a> 							| //schema-element(tn-ra:RailwayStationNode)
RailwayYardNode <a name="RailwayYardNode"></a> 									| //schema-element(tn-ra:RailwayYardNode)



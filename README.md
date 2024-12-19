# Shared Care Record Patient Summaries - Draft Specification

This is an initial draft of a proposed specification of a shared care record summary, aligning with the [FHIR International Patient Summary](https://build.fhir.org/ig/HL7/fhir-ips/index.html), and focusing on a data-set designed to support urgent care use-cases.

For this specification, the STU2 release (2.0.1) of [UK Core](https://simplifier.net/guide/UKCoreVersionHistory/Home?version=current) was used for the profiles to apply to resources returned, in combination with those defined in the FHIR International Patient Summary specification. Once it is stable, the later STU3 (or later) release of UK Core should be used, but at the time of writing this specification, the STU3 release (1.7.0) has errors in profiles making it unsuitable for use currently.

## Contents

 * [Assumptions](Assumptions.md)
 * [Document Information](DocumentInformation.md)
 * [Required Data Items](RequiredDataItems.md)
 * [Recommended Data Items](RecommendedDataItems.md)
 * [Required Data Items](RequiredDataItems.md)
 * [Narrative Content in IPS](NarrativeInIPS.md)
 * [HTML/PDF Representation](HTMLPDF.md)
 * [API to Generate IPS](API.md)
 * [Summary Record Pointer in NRL](NRL.md)
 * [Example Summaries](Examples.md)
 * [Open Questions / Clarifications](OpenQuestions.md)
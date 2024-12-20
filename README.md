# Shared Care Record Patient Summaries - Draft Specification

This is an initial draft of a proposed specification of a shared care record summary, aligning with the [FHIR International Patient Summary](https://build.fhir.org/ig/HL7/fhir-ips/index.html), and focusing on a data-set designed to support urgent care use-cases.

For this specification, the STU2 release (2.0.1) of [UK Core](https://simplifier.net/guide/UKCoreVersionHistory/Home?version=current) was used for the profiles to apply to resources returned, in combination with those defined in the FHIR International Patient Summary specification. Once it is stable, the later STU3 (or later) release of UK Core should be used, but at the time of writing this specification, the STU3 release (1.7.0) has errors in profiles making it unsuitable for use currently.

Unless otherwise stated in this specification, all requirements outlined in the [FHIR International Patient Summary](https://build.fhir.org/ig/HL7/fhir-ips/index.html) implementation guide should be adhered to. The purpose of this guide is to add additional context and requirements around how this guide is applied to this use-case.

## Contents

 1. [Assumptions](01-Assumptions.md)
 2. [Document Information](02-DocumentInformation.md)
 3. [Required Data Items](03-RequiredDataItems.md)
 4. [Recommended Data Items](04-RecommendedDataItems.md)
 5. [Optional Data Items](05-OptionalDataItems.md)
 6. [Narrative Content in IPS](06-NarrativeInIPS.md)
 7. [HTML/PDF Representation](07-HTMLPDF.md)
 8. [API to Generate IPS](08-API.md)
 9. [Summary Record Pointer in NRL](09-NRL.md)
 10. [Example Summaries](10-Examples.md)
 11. [Open Questions / Clarifications](11-OpenQuestions.md)
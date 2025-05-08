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
 6. [Limits on Data Returned](06-LimitsOnDataReturned.md)
 7. [Narrative Content in IPS](07-NarrativeInIPS.md)
 8. [HTML/PDF Representation](08-HTMLPDF.md)
 9. [API to Generate IPS](09-API.md)
 10. [Summary Record Pointer in NRL](10-NRL.md)
 11. [Example Summaries](11-Examples.md)
 12. [Mapping To Urgent Care Dataset](12-MappingToUrgentCareDataset.md)
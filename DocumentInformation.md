# Document Information

The below table provides details of how to populate key items from the urgent care data-set into the International Patient Summary FHIR Bundle

## Composition

The composition is the overarching document which provides the context, and groups the content into sections to represent the sections defined in the IPS specification.

 * Filters/Constraints: N/A
 * FHIR Resource Profiles to conform to:
   * [Composition (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/Composition-uv-ips)

Example:
* [Example FHIR Composition]()
* [Example HTML Narrative](https://html-preview.github.io/?url=https://github.com/ahatherly-gn/NHS-SCR-IPS/blob/main/Examples/Narrative-Composition.html)

NOTE: The composition sections each include narrative for the section - examples of this narrative for each section are described in the relevant sections of this specification for each IPS section.

## Patient

This is a set of demographics for the patient. Where the patient has multiple versions of demographics, the "golden" record, or the demographics that are traced and aligned to PDS should be used.

 * Filters/Constraints: N/A
 * FHIR Resource Profiles to conform to:
   * [UKCore-Patient](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Patient?version=2.0.1)
   * [Patient (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/Patient-uv-ips)

Example:
* [Example FHIR Patient](Examples/Patient.json)

## Author

The expectation is that the summary will be created on-demand by the shared care record, so the author in this case is a "Device" representing the shared care record that generated the summary.

* Filters/Constraints: N/A
 * FHIR Resource Profiles to conform to:
   * Base FHIR Device Profile

Example:
* [Example FHIR Device](Examples/Author-Device.json)

## Attester

The expectation is that the summary will be created on-demand by the shared care record, so would not have an attester, so this will not be populated.

## Custodian

Not required as typically the shared record included data from a range of orgnisations, so there is no single custodian.
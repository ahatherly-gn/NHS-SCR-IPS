# Document Information

The below table provides details of how to populate key items from the urgent care data-set into the International Patient Summary FHIR Bundle

## Composition



## Patient

This is a set of demographics for the patient. Where the patient has multiple versions of demographics, the "golden" record, or the demographics that are traced and aligned to PDS should be used.

 * Filters/Constraints: N/A
 * FHIR Resource Profiles to conform to:
   * [UKCore-Patient](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Patient?version=2.0.1)
   * [Patient (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/Patient-uv-ips)

## Author

The expectation is that the summary will be created on-demand by the shared care record, so the author in this case is a "Device" representing the shared care record that generated the summary.

* Filters/Constraints: N/A
 * FHIR Resource Profiles to conform to:
   * Base FHIR Device Profile

## Attester

The expectation is that the summary will be created on-demand by the shared care record, so would not have an attester, so this will not be populated.

## Custodian

Not required as typically the shared record included data from a range of orgnisations, so there is no single custodian.
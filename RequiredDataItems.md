# Required Data Items

The below list provides details of how to populate key items from the urgent care data-set into the International Patient Summary FHIR Bundle

## Problems

Items recorded as "problems" in local clinical systems (e.g. items on the problems list in primary care). In addition, where possible, any other coded items from the record that have codes that indicate that they are conditions or disorders.

 * Filters/Constraints
   * Where there is a status, include only those that are "active"
 * FHIR Resource Profiles to conform to:
   * [UKCore-Condition](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Condition?version=2.0.1)
   * [Condition (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/Condition-uv-ips)

Example:

* [Example FHIR Condition](Examples/Condition.json)
* [Example HTML Narrative](https://html-preview.github.io/?url=https://github.com/ahatherly-gn/NHS-SCR-IPS/blob/main/Examples/Narrative-Problems.html)

## Allergies and Intolerances

Items recorded as "Allergies" in local clinical systems.

 * Filters/Constraints
   * Include ALL where status="active"
 * FHIR Resource Profiles to conform to:
   * [UKCore-AllergyIntolerance](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-AllergyIntolerance?version=2.0.1)
   * [AllergyIntolerance (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/AllergyIntolerance-uv-ips)

## Medication Summary

Current medications being taken. This includes active prescribed medications, including repeat, one-off and acute meds and any meds recorded in other care settings if available.

 * Filters/Constraints
   * Include ALL where status="active"
 * FHIR Resource Profiles to conform to:
   * [UKCore-MedicationStatement](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-MedicationStatement?version=2.0.1)
   * [MedicationStatement (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/MedicationStatement-uv-ips)

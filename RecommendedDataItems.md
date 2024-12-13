# Recommended Data Items

The below list provides details of how to populate key items from the urgent care data-set into the International Patient Summary FHIR Bundle

## Immunisations

This will include any Immunisation records - typically from primary care, but can be from other care settings.

* Filters/Constraints
   * All immunisations with status="completed"
* FHIR Resource Profiles to conform to:
   * [UKCore-Immunization](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Immunization?version=2.0.1)
   * [Immunization (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/Immunization-uv-ips)


## Results

This will be a combination of results that are included in a DiagnosticReport (e.g. Acute Pathology results), and some individual coded Observations that are not part of a report (e.g. results taken from the GP record)

* Filters/Constraints
   * Where possible, apply different time-ranges based on the type of result
     * Biochemistry: Last 6 months
     * Haematology: Last 6 months
     * Immunology: Last 6 months
     * Microbiology: Last 12 months
     * Virology: Last 12 months
     * Histology: Entire history
     * Cytology: Entire history
     * Other/Unknown: Last 12 months
* FHIR Resource Profiles to conform to:


## History of Procedures


## Medical Devices



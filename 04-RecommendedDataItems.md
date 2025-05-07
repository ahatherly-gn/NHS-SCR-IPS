# Recommended Data Items

The below list provides details of how to populate key items from the urgent care data-set into the International Patient Summary FHIR Bundle

## Immunisations

This will include any Immunisation records - typically from primary care, but can be from other care settings.

* Filters/Constraints
   * All immunisations with status="completed"
* FHIR Resource Profiles to conform to:
   * [UKCore-Immunization](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Immunization?version=2.0.1)
   * [Immunization (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/Immunization-uv-ips)

Example:

* [Example FHIR Immunization](Examples/Immunization.json)
* [Example HTML Narrative](https://html-preview.github.io/?url=https://github.com/ahatherly-gn/NHS-SCR-IPS/blob/main/Examples/Narrative-Immunisations.html)

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
   * Otherwise (or for other types of result): Last 12 months
* FHIR Resource Profiles to conform to:
   * [UKCore-Observation](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Observation?version=2.0.1)
   * [UKCore-Observation-Lab](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Observation-Lab?version=2.0.1)
   * [UKCore-Observation-Group-Lab](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Observation-Group-Lab?version=2.0.1)
   * [UKCore-DiagnosticReport](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-DiagnosticReport?version=2.0.1)
   * [UKCore-DiagnosticReport-Lab](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-DiagnosticReport-Lab?version=2.0.1)
   * [DiagnosticReport (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/DiagnosticReport-uv-ips)
   * [Observation Results (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/Observation-results-uv-ips)

**Relevant items from NHSE Urgent Care Dataset**:

 * Data Item: Diagnostics
   * PRSB: CIS Investigation Results
   * Must have data items:
      * Investigation -coded value
      * Investigation - free text
      * Investigation result - coded value
      * Investigation result - free text
      * Structured investigation result - value, units of measure, reference ranges, abnormal indicator
 * Data Item: Observations (Current - time/event period needs defining)
   * PRSB: CIS Examination findings
 * Data Item: ECG
   * PRSB: CIS Investigation Results
   * Must have data items:
      * As above for CIS Investigation Results

**Example:**

* Examples to be added

## History of Procedures

This will be all Procedures in the record with a date in the past.
>Question: Should we limit this to the last X procedures? There could be an awful lot if we go back forever

* Filters/Constraints
   * All Procedures with performedDateTime or performedPeriod.end before today (or without a performedDateTime/performedPeriod value)
* FHIR Resource Profiles to conform to:
   * [UKCore-Procedure](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Procedure?version=2.0.1)
   * [Procedure (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/Procedure-uv-ips)

**Example:**

* Examples to be added

## Medical Devices

It is unlikely that this information would be held in a shared care record, but if it is, it can be included as a list of FHIR Device resources.

* Filters/Constraints
   * All devices with status="active"
* FHIR Resource Profiles to conform to:
   * [Device (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/Device-uv-ips)

**Example:**

* N/A
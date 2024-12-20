# Optional Data Items

The below table provides details of how to populate key items from the urgent care data-set into the International Patient Summary FHIR Bundle

## Advance Directives

This should be any Observations in the record which relate to the existence of other key document such as EPaCCS forms or ReSPECT forms - these actual documents should be separate pointers on NRL, so should not be replicated into this summary document, rather this should indicate their existence so the user can review and retrieve them separately from NRL.

In addition, this section of the summary could contain any other specific key coded observations from those documents, such as ADRT/CPR decisions.

* Filters/Constraints
   * Observations that relate to advanced directives, or the existence of documents like EPaCCS or ReSPECT forms, etc.
   * Items in narrative should be sorted newest to oldest based on recorded date
 * FHIR Resource Profiles to conform to:
   * [UKCore-Observation](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Observation?version=2.0.1)

Example:

* Examples to be added

## Functional Status

Observations containing any functional assessment scores - e.g. Frailty score, Rockwood score. Potentially any other coded observations that relate to functional status.

* Filters/Constraints
   * Observations that relate to functional status, or assessment scores relating to functional status
   * Items in narrative should be sorted newest to oldest based on recorded date
 * FHIR Resource Profiles to conform to:
   * [UKCore-Observation](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Observation?version=2.0.1)

Example:

* Examples to be added

## History of Pregnancy 

Episodes of care that relate to pregnancies - with dates, and any associated observations relating to due dates, outcomes and pregancy status.

* Filters/Constraints
   * Episodes of care that relate to pregnancy episodes
   * Observations with codes that relate to expected due dates, outcomes and pregnancy status
   * Items in narrative should be sorted newest to oldest based on recorded date
 * FHIR Resource Profiles to conform to:
   * [UKCore-Observation](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Observation?version=2.0.1)
   * [Observation Pregnancy - Expected Delivery Date (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/Observation-pregnancy-edd-uv-ips)
   * [Observation Pregnancy - Outcome (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/Observation-pregnancy-outcome-uv-ips)
   * [Observation Pregnancy - Status (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/Observation-pregnancy-status-uv-ips)

Example:

* Examples to be added

## Plan of Care

Care plan documents should be shared as separate documents with NRL, so shoud not be included in the shared record patient summary document.

## Alerts

Any active alerts held against the patient. This could include items explicitly created as alerts and any other coded items relating to safeguarding or other items deemed clinically significant enough to flag as alerts.

* Filters/Constraints
   * Flags relating to items explicitly created as "alerts", plus any other items deemed clinically significant - e.g. safeguarding information
   * Items in narrative should be sorted newest to oldest based on recorded date
 * FHIR Resource Profiles to conform to:
   * [Flag - Alert (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/Flag-alert-uv-ips)
   
Example:

* Examples to be added

## History of Past Problems

Items recorded as "problems" in local clinical systems (e.g. items on the problems list in primary care) that are not "active"

 * Filters/Constraints
   * Include where status is NOT "active"
   * Items in narrative should be sorted newest to oldest based on recorded date
 * FHIR Resource Profiles to conform to:
   * [UKCore-Condition](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Condition?version=2.0.1)
   * [Condition (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/Condition-uv-ips)

Example:

* Examples to be added

## Patient Story (AKA About Me)

About Me documents should be shared as separate documents with NRL, so shoud not be included in the shared record patient summary document.

## Social History

Any observations in the record which relate to smoking or alcohol use.

* Filters/Constraints
   * Observations with codes that relate to smoking or alcohol use
   * Items in narrative should be sorted newest to oldest based on recorded date
* FHIR Resource Profiles to conform to:
   * [UKCore-Observation](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Observation?version=2.0.1)
   * [Observation Social History - Alcohol Use (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/Observation-alcoholuse-uv-ips)
   * [Observation Social History - Tobacco Use (IPS)](http://hl7.org/fhir/uv/ips/StructureDefinition/Observation-tobaccouse-uv-ips)

Example:

* Examples to be added

## Vital Signs

Observations from the record with codes that indicate they relate to vital signs.

* Filters/Constraints
   * Where possible, apply different time-ranges for the effective date of the Observation based on the type of result
     * Blood pressure readings (last 6 months)
     * O2 saturations (last 6 months)
     * Heart Rate (last 6 months)
     * Height / Weight / BMI (Latest only)
   * Where this is not possible, limit the data to the last 6 months
   * Items in narrative should be grouped by type, and within each type, sorted newest to oldest based on recorded date
* FHIR Resource Profiles to conform to:
   * [UKCore-Observation](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Observation?version=2.0.1)

Example:

* Examples to be added

## Social Care

Flag to indicate if the patient is known to social care

* Filters/Constraints
  * Derived flag to incidate that the patient is known to social care based on data about social care being available in the shared record
* FHIR Resource Profiles to conform to:
   * Base FHIR Flag Profile

Example:

* Examples to be added

## Encounters

Future Encounters (e.g. Acute Waiting Lists), plus the last 6 months of previous encounters

* Filters/Constraints
   * Encounter records that have a start date greater than 6 months ago
   * Items in narrative should be sorted newest to oldest based on start date
* FHIR Resource Profiles to conform to:
   * [UKCore-Encounter](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Encounter?version=2.0.1)

Example:

* Examples to be added

## Legal information (PoA)

Lasting power of attorney information where this is recorded in the shared record. This could either be a related person or an observation that a power of attorney has been appointed

* Filters/Constraints
   * RelatedPerson records with a type that indicates they are a Power of Attorney, or any Observations with codes that indicate they relate to power of attorneys
   * Items in narrative should be sorted newest to oldest based on start date
* FHIR Resource Profiles to conform to:
   * [UKCore-RelatedPerson](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-RelatedPerson?version=2.0.1)
   * [UKCore-Observation](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Observation?version=2.0.1)

Example:

* Examples to be added
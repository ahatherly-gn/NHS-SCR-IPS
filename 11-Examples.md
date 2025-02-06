# Examples

Below are some examples of a complete FHIR IPS Document, and also snippets of the individual FHIR Resources and Narrative content within the overall document (these snippets are also included in the relevent sections of this guide).

## Overall IPS Example

[Sample International Patient Summary FHIR Bundle](Examples/SCRSummary.json)

Note: This example can be pasted into [this web site](https://www.ipsviewer.com/) to show the content and give an idea about how it could be rendered.

## Individual Sections/Resources

|Section | FHIR Resource(s)  | FHIR Example | Narrative Example |
|--------|-----------|--------------|-------------------|
| Document Information | Composition | [Example FHIR Composition](Examples/Composition.json) | [Example HTML Narrative](https://html-preview.github.io/?url=https://github.com/ahatherly-gn/NHS-SCR-IPS/blob/main/Examples/Narrative-Composition.html)
| Patient | Patient | [Example FHIR Patient](Examples/Patient.json) | |
| Author | Device | [Example FHIR Device](Examples/Author-Device.json) | |
| Problems | Conditions | [Example FHIR Condition](Examples/Condition.json) | [Example HTML Narrative](https://html-preview.github.io/?url=https://github.com/ahatherly-gn/NHS-SCR-IPS/blob/main/Examples/Narrative-Problems.html) |
| Allergies and Intolerances | AllergyIntolerance | [Example FHIR AllergyIntolerance](Examples/AllergyIntolerance.json) | [Example HTML Narrative](https://html-preview.github.io/?url=https://github.com/ahatherly-gn/NHS-SCR-IPS/blob/main/Examples/Narrative-Allergies.html) |
| Medication Summary | MedicationStatement | [Example FHIR MedicationStatement](Examples/MedicationStatement.json) | [Example HTML Narrative](https://html-preview.github.io/?url=https://github.com/ahatherly-gn/NHS-SCR-IPS/blob/main/Examples/Narrative-Medications.html) |
| Immunisations | Immunization | [Example FHIR Immunization](Examples/Immunization.json) | [Example HTML Narrative](https://html-preview.github.io/?url=https://github.com/ahatherly-gn/NHS-SCR-IPS/blob/main/Examples/Narrative-Immunisations.html) |
| Results | DiagnosticReport, Observation | | |
| History of Procedures | Procedure | | |
| Medical Devices | Device | | |
| Advance Directives | | | |
| Functional Status | | | |
| History of Pregnancy  | | | |
| Plan of Care | | | |
| Alerts | | | |
| History of Past Problems | | | |
| Patient Story (AKA About Me) | | | |
| Social History | | | |
| Vital Signs | | | |
| Social Care | | | |
| Encounters | | | |
| Legal information (PoA) | | | |

# Examples

Below are some examples of a complete FHIR IPS Document, and also snippets of the individual FHIR Resources and Narrative content within the overall document (these snippets are also included in the relevent sections of this guide).

## Overall IPS Example

[Sample International Patient Summary FHIR Bundle](Examples/SCRSummary.json)

Note: This example can be pasted into [this web site](https://www.ipsviewer.com/) to show the content and give an idea about how it could be rendered.

## Individual Sections/Resources

|Section | FHIR Resource(s)  | FHIR Example | Narrative Example |
|--------|-----------|--------------|-------------------|
| Document Information | Composition | [Composition](Examples/Composition.json) | [HTML Narrative](https://html-preview.github.io/?url=https://github.com/ahatherly-gn/NHS-SCR-IPS/blob/main/Examples/Narrative-Composition.html)
| Patient | Patient | [Patient](Examples/Patient.json) | |
| Author | Device | [Device](Examples/Author-Device.json) | |
| Problems | Conditions | [Condition](Examples/Condition.json) | [HTML Narrative](https://html-preview.github.io/?url=https://github.com/ahatherly-gn/NHS-SCR-IPS/blob/main/Examples/Narrative-Problems.html) |
| Allergies and Intolerances | AllergyIntolerance | [AllergyIntolerance](Examples/AllergyIntolerance.json) | [HTML Narrative](https://html-preview.github.io/?url=https://github.com/ahatherly-gn/NHS-SCR-IPS/blob/main/Examples/Narrative-Allergies.html) |
| Medication Summary | MedicationStatement | [MedicationStatement](Examples/MedicationStatement.json) | [HTML Narrative](https://html-preview.github.io/?url=https://github.com/ahatherly-gn/NHS-SCR-IPS/blob/main/Examples/Narrative-Medications.html) |
| Immunisations | Immunization | [Immunization](Examples/Immunization.json) | [HTML Narrative](https://html-preview.github.io/?url=https://github.com/ahatherly-gn/NHS-SCR-IPS/blob/main/Examples/Narrative-Immunisations.html) |
| Results | DiagnosticReport, Observation | [DiagnosticReport](Examples/Result-DiagnosticReport.json) [Parent Observation](Examples/Result-ParentObservation.json) [Observation 1](Examples/Result-ChildObservation1.json) [Observation 2](Examples/Result-ChildObservation2.json) | [HTML Narrative](https://html-preview.github.io/?url=https://github.com/ahatherly-gn/NHS-SCR-IPS/blob/main/Examples/Narrative-Results.html) |
| History of Procedures | Procedure | [Procedure](Examples/Procedure.json) | [HTML Narrative](https://html-preview.github.io/?url=https://github.com/ahatherly-gn/NHS-SCR-IPS/blob/main/Examples/Narrative-Procedures.html) |
| Medical Devices | Device | N/A | N/A |
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

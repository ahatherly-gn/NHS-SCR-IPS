# Narrative Content in the IPS

According to the [IPS Specification](https://build.fhir.org/ig/HL7/fhir-ips/Design-Conventions.html):

> The IPS Composition includes a requirement for each section to have human-readable narrative text. This includes the 16 clinical sections profiled in the IPS Composition as well as any other section included in the patient summary.

But also advises:

> While no constraints are implemented, early implementers have recommended that IPS documents not duplicate the content contained in Composition.section.text (which is required) in the Composition.text

Narrative may be created with human intervention, but it is likely that some form of automated generation may be used in most shared care records. The IPS specification does not dictate how this should be done or what data from the FHIR resources should be considered clinically relevant for inclusion, so this is left for the implementers to determine. There is, however, some guidance provided in the IPS specification for areas such as person names and medication lists.

For the purposes of the Shared Care Record Patient Summary, the narrative components will be populated as follows:

* The demographic information about the patient MUST be populated in the narrative within the Patient resource in the bundle
* The IPS Composition's narrative section MUST contain the basic data from the composition - including the title, the date the summary was generated, and the author (which will be the name of the shared record that the summary was generated from)
* The IPS Composition contains a collection of the document sections, each of which has references to the FHIR resources, but also has a textual representation (in the form of HTML) - this MUST hold the human-readable rendering of the key information from the section - typically in the form of a HTML table of the clinical items in the section
* There is no requirement for any other FHIR resources in the bundle to include narrative content - all relevant information that would be required for human review of the summary is included in the above narrative content
* English spellings should be used rather than American-English in narrative sections - i.e. "Immunisation" rather than "Immunization"

Narrative content should be:
*  **Concise and clinically relevant**: Narratives should summarise the key clinical facts without duplicating all structured data.
* **Human-readable**: They must be understandable by clinicians without requiring parsing of the underlying FHIR resources.
* **Synchronised with data**: The data in the narrative must accurately reflect the structured data in the section.

## Best Practices for populating narrative content

IPS generators often use default narrative templates for each section. These templates:

* Are typically HTML-based.
* Are populated using the FHIR resources relevant to each section.
* Ensure consistency and readability across implementations.

Examples of how narrative content could look for IPS sections, please refer to the [examples](11-Examples.md) section.

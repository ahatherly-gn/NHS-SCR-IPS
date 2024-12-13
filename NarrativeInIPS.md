According to the [IPS Specification](https://build.fhir.org/ig/HL7/fhir-ips/Design-Conventions.html):

> The IPS Composition includes a requirement for each section to have human-readable narrative text. This includes the 16 clinical sections profiled in the IPS Composition as well as any other section included in the patient summary.

But also advises:

> While no constraints are implemented, early implementers have recommended that IPS documents not duplicate the content contained in Composition.section.text (which is required) in the Composition.text

Narrative may be created with human intervention, but it is likely that some form of automated generation may be used in most shared care records. The IPS specification does not dictate how this should be done, or what data from the FHIR resources should be considered clinically relevant for inclusion, so this is left for the implemeters to determine. There is however some guidance provided in the IPS specification for areas such as person names and medication lists.


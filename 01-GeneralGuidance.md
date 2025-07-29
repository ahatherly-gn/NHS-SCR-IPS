# General Guidance

 * FHIR R4 will be used as the base FHIR version
 
 * Wherever possible codes should be SNOMED, but for England International Patient Summaries, this will use codes from the full UK SNOMED release and **WILL NOT** be limited to the ["IPS Terminology"](https://www.snomed.org/international-patient-summary-terminology) subset created by SNOMED International for use in international summaries.

 * FHIR Resources included in the IPS bundle **SHOULD** conform to UK Core profiles as well as the relevant profiles within the International Patient Summary implementation guide.

* The source Shared Care Record **MUST** return all relevant data from their ShCR, as per the agreed specification, regardless of potential duplication at the consumer end.

* Source shared care records **SHOULD** return data equivalent to what is provided locally within their own systems.

* Where data is structured, de-duplication **SHOULD** be handled by the consumer system (e.g. Shared care records or NCRS - when ready)

* Where additional patient information is available from the Spine or other external shared records, there is no requirement for the Shared Care Record generating the summary to attempt to retrieve and incorporate this into the summary that is generated.

* IPS documents **WILL NOT** include meta.profile attributes when sent over the wire. They may be included in examples in this guide to allow for validation and testing, but would not be included in IPS documents generated in live systems.

* Composition sections **MUST** be LOINC coded [as per the IPS spec](https://build.fhir.org/ig/HL7/fhir-ips/StructureDefinition-Composition-uv-ips.html), and will use the fixed LOINC codes defined in that specification.
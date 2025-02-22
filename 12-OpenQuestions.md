# Open Questions

There are a number of open questions and clarifications still to be resolved in relation to this draft specification:

- The Composition in the IPS has a "period" for the document (within the "Event" element) which is marked as "must support". It is not clear how this would be populated, and if implementers would need to analyse all data in the summary to determine the earliest and latest data items to reflect in this period. This would be a high overhead, and it isn't clear whether this is actually required for the NHS SCR Summary.

- The UK Core MedicationStatement profile states that the "derivedFrom" should be provided, which links the MedicationStatement to the MedicationRequest, but it is not clear that this would be a useful inclusion in an urgent care summary. A similar query applies to the "basedOn" reference. If these are references to a FHIR ReST URL within the shared care record, it it not clear how/if clients would be able to (or want to) be able to separately resolve and retrieve these, so if they are needed it is to be assumed that they would also need to be included in the IPS bundle, making it potentially significantly larger.

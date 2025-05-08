# Mapping to Urgent Care Dataset

NHS England held a workshop with clinicians to identify a core dataset for urgent care. This forms the basic requirement for the data to be included in this International Patient Summary.

This was provided as an Excel Spreadsheet - the original of which is available [here](Files/Prototype%20clinical%20data%20requirements.xlsx)

The below table shows the items from that initial data-set, and how each maps (or doesn't) to the relevant sections in the FHIR International Patient summary in this guide.

## Common Core Data Items

| Item | PRSB | Must Have Data Items | Mapping to IPS Section | Comments |
|------|------|----------------------|-------------------|----------|
| Demographics (National PDS) | CIS Demographics | Person first name, Person family name, NHS number, Address lines 1-5 and postcode, Telephone number, Telephone number type | [Document Information](02-DocumentInformation.md): Patient | 
| DNAR | CIS Legal information | Advance decision to refuse treatment (ADRT), Date OR Alert flag and associated free text | [Optional Items](05-OptionalDataItems.md): Advance Directives | 
| | CIS End of life care | CPR Decision date and time, CPR decision coded value, CPR decision free text, CPR decision date for review, CPR decision location of document | [Optional Data Items](05-OptionalDataItems.md): Advance Directives |  
| Safeguarding | CIS Safeguarding | Safeguarding indicator, Safeguarding concerns date, Safeguarding concerns end date | [Optional Items](05-OptionalDataItems.md): Alerts | 
| Medication (Current GP Meds and Discharge Meds) | CIS Medications | Medication name - coded value. Medication name - free text | [Required Items](02-DocumentInformation.md): Medication Summary | 
| Allergies | CIS Allergies | Causative agent  - coded value, Causative agent - free text, Type of reaction, Description of reaction - coded value, Description of reaction - free text | [Required Items](02-DocumentInformation.md): Allergies and Intolerances | 
| Diagnostics | CIS Investigation Results | Investigation -coded value, Investigation - free text, Investigation result - coded value, Investigation result - free text, Structured investigation result -value, units of measure, reference ranges, abnormal indicator | [Recommended Items](04-RecommendedDataItems.md): Results | 
| Reasonable Adjustments (Spine API) | CIS Individual Requirements | Resonable adjustment flag, Impairment category - coded value, Impairment cateogory - free text | NOT INCLUDED | Already provided from Spine - Probably shouldn't be replicated into this summary?
| Care Plans | PCSP, Or if surfacing as documents then CIS Documents | Document title, Document date | NOT INCLUDED | Should be shared as separate items on NRL rather than in this summary? 
| Observations (Current - time/event period needs defining) | CIS Examination findings | CIS does not specify any must have data items for examination findings | [Recommended Items](04-RecommendedDataItems.md): Results | 
| Known to Social Care (Current Social Care Support + provider) | CIS Services and Care | Social care package name, Social care package type, Service start date, Service end date, Local authority - coded value, Local authorty - free text | [Optional Items](05-OptionalDataItems.md): Social Care | 
| ECG | CIS Investigation Results | Investigation -coded value, Investigation - free text, Investigation result - coded value, Investigation result - free text, Structured investigation result -value, units of measure, reference ranges, abnormal indicator, May be surfaced as a document: Document title, Document date | [Recommended Items](04-RecommendedDataItems.md): Results | 

## Additional Data Items

| Item | PRSB | Must Have Data Items | Mapping to IPS Section | Comments |
|------|------|----------------------|-------------------|----------|
| Discharge notes/letters  (Recent - time/event period needs defining) | If surfacing as documents then CIS Documents | Document title, Document date | NOT INCLUDED | Unclear how copies of discharge summary documents could be included in a patient summary?
| Encounters (Recent - time/event period needs defining) | CIS Admission details | Date of admission, Admitted to  - organisation code, Admitted to - organisation free text, Specialty - activity treatment function code, Specialty - free text, Reason for admission - code, Reason for admission - free text, Legal status on admission - code | [Optional Items](05-OptionalDataItems.md): Encounters | 
| | CIS Discharge details | Date of discharge, Discharge location - ods code, Discharging specialty - code, Discharging specialty - free text, Legal status on discharge, Discharge destination - code, Discharge destination - address -free text | [Optional Items](05-OptionalDataItems.md): Encounters | 
|  | CIS Contacts with professionals | CIS does not specify any must have data items for contacts with professionals. | NOT INCLUDED | Unclear what this would be?
| Maternity status (no. of weeks pregnant) | CIS Pregnancy status | Pregnancy state - yes/no, Expected delivery date | [Optional Items](05-OptionalDataItems.md): History of Pregnancy | 
| Access |  |  | NOT INCLUDED | Unclear what this means
| Social history | CIS Social Context | CIS does not specify any must have data items for social context | [Optional Items](05-OptionalDataItems.md): Social History | 
| About Me | About Me | About Me - must be maintained and surfaces as a single file and contains: What's most imnportant to me. People who are important to me, How I communicate and how to communicate with me, My wellness, How and when to support me, Also worth knowing about me, Supported to write this by, Date | NOT INCLUDED | Should be shared as separate item on NRL rather than in this summary?
| Known to Social Care (Current Social Care Support + provider) |  |  |  | Duplicate - covered in duplicate item above
| NOK/POA - New Term | CIS Legal information, CIS Personal Contacts | Lasting Power of Attorney for health and welfare - coded, Location of document, Name of LPA, Contact details | [Optional Items](05-OptionalDataItems.md): Legal Information (PoA) | 
| Imaging Reports (Inc. dates and contect) |  |  | NOT INCLUDED | Separate initiative for sharing of imaging reports, should be used rather than this summary?
| Baseline Data |  |  |  | Unclear what this means
| Appointments (upcoming) | CIS Future Appointments | Date of appointment, Location of future appointment - code, Location of future appointment - free text, Specialty - treatment function code | NOT INCLUDED | Should be sourced from Wayfinder rather than this summary?
| Conditions (Current active and significant past) | CIS Problem List | Problem - code, Problem - free text, Problem onset date, Problem end date | [Required Items](03-RequiredDataItems.md): Problems | 
| Pre- contact information e.g. scene safety (covered in demographics?) | CIS Problem List | Problem - code, Problem - free text, Problem onset date, Problem end date | [Optional Items](05-OptionalDataItems.md): Alerts | 
| ADRT |  |  |  | Duplicate - covered in DNAR item above

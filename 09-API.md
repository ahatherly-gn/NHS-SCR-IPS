# API Implementation

The FHIR IPS Implementation Guide suggests two potential options for how an IPS could be requested:

- Using a $summary operation on the Patient resource
- Using a $docref operation on a DocumentReference resource

However, to provide a consistent interface for clients, and to avoid them having to query the CapabilityStatement of the server to establish what is supported (for which there is no simple standard route currently), all implementers MUST support a GET using the $summary operation on the patient resource as per the below example:

```
GET https://fhirbaseurl/Patient/12345/$summary
Content-Type: application/fhir+json
```

The base URL can be anything, and would be determined by the implementer (there is no requirement for the base URL to be consistent across patients, even within the same shared record).

The format of summary returned will be determined by the Content-Type in the GET request. All implementations should support the following three content types:

- **Content-Type: application/fhir+xml** - This will return an XML formatted IPS FHIR Bundle
- **Content-Type: application/fhir+json** - This will return a JSON formatted IPS FHIR Bundle
- **Content-Type: text/html** - This will return a HTML representation of the summary document

In addition, an implementation may optionally support:

- **Content-Type: application/pdf** - This will return a PDF representation of the summary document

See [this page](08-HTMLPDF.md) for details of HTML/PDF representations.

This approach assumes that there is a single type of summary document made available via this route, which will be the urgent care summary. In future, if there is a requirement for other types of summary, then another type of request/pointer will need to be used, with a separate DocumentReference lodged in NRL. This may use the $docref approach, with a parameter in the request to specify the type of summary being requested, or it could potentially be supported using different custom operations or parameters in the $summary operation. The details of how this would be implemented are for future consideration and are out of scope of this specification.

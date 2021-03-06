# Notes

Assorted findings that need further processing to make sense of them

## Documentation
There needs to be a lot more, and better structured. So one thing to get right from the start is Requirements Engineering (Gathering, Tracking, & Specification)

### ReqEng
* http://stackoverflow.com/questions/171653/examples-of-requirement-documents
* http://techwhirl.com/writing-software-requirements-specifications/
* https://en.wikipedia.org/wiki/Software_requirements_specification

## UI

Consider shift of methodolgy as shown by the OPAL project, using Angluar JS as the Client side technology, with a Django application service backing it (and possibly a direct link to FhirBase?)

* https://angular.io/docs/ts/latest/guide/architecture.html
* http://www.bluebuttonjs.com -- BlueButton.js helps developers parse and generate complex health data formats like C-CDA with ease, so you can empower patients with access to their health records.
* https://github.com/openhealthcare/opal -- Django+Angular OSS health system
 * With Plugins (though none for Transplant): http://opal.openhealthcare.org.uk/docs/guides/plugins_list/
 * Documentation: http://opal.openhealthcare.org.uk/docs/


## Data Structures

There are many :-/

### NHS

* NHS HSCIC has a data dictionary, with contents online at: http://www.datadictionary.nhs.uk/data_dictionary/diagrams/diagrams/person_diagram_fr.asp?shownav=1
* https://data.england.nhs.uk -- Find and explore the data used by NHS England to conduct its core business
* http://systems.digital.nhs.uk/ddc -- Are behind the NHS Spine
* https://code4health.org -- An incubator group from NHS England
* There are many references to strategy and ongoing work via the NHS Digital Technology pages - https://www.england.nhs.uk/digitaltechnology/
* Various data resources can be found on the TRUD (the Technology Reference data Update Distribution site) - https://isd.hscic.gov.uk/trud3/user/guest/group/0/home
 * Look for the UK SNOMED CT! - https://isd.hscic.gov.uk/trud3/user/guest/group/0/pack/26
 * The Interoperability Toolkit - https://isd.hscic.gov.uk/trud3/user/guest/group/41/pack/30

### Fhir(base)

A likely favourite as their data model seems more flexible and saner (see person -> names as an example compared to NHS)

* http://fhirbase.github.io -- Docs
* https://github.com/fhirbase -- Code repositories
* https://github.com/fhirbase/fhirbase-plv8 -- Repository for the Postgres Implementation
* http://fhirbase.github.io/demo/index.html -- Demo site with query window


* http://hl7.org/implement/standards/fhir/documentation.html -- Fhir documentation
* http://hl7.org/implement/standards/fhir/datatypes.html -- Fhir datatypes
* http://hl7.org/implement/standards/fhir/resourcelist.html -- Fhir resource types
* http://hl7.org/implement/standards/fhir/resourceguide.html -- HL7 standards
* http://hl7.org/implement/standards/fhir/implementation.html -- Fhir implementation checklist

* http://www.hl7.org.uk/doc_store/NHS/HL7%20Integration%20Options%20for%20Trusts.pdf -- HL7 talks about integration strategies, including the need for roadmaps (and steps to create)

* http://www.ehealthnews.eu/emis/4679-emis-health-implements-open-standards-for-interoperability -- EMIS are using Fhirbase with Snomed and NHS DD

* http://stackoverflow.com/questions/tagged/hl7-fhir -- Stackoverflow has 260 Q&As so far

* From GNU Health, there's a python reference library for Fhir: https://pypi.python.org/pypi/fhir

* Someone is having a go at merging Django with other techs to get a Fhir stack: https://github.com/videntity/django-fhir

* Or from SMARTonFHIR: https://github.com/smart-on-fhir/client-py

### OpenEHR

Scotland went a different way earlier on and supported the Open EHR initiative, something started at UCL, but now international. 

* http://www.openehr.org/home


## Infrastructure

At somepoint, the reality is that developed services will need to operate somewhere. Given the low value and high cost of IM&T solutions, external alternatives to consider include:

* Searching for "g cloud nhs accredited n3 hosting":
* http://www.redcentricplc.com/services/infrastructure/hosting-colocation/n3-hosting/
* https://www.4d-dc.com/cloud
* http://ukcloud.com -- The new name for Skyscape
 * Supposedly behind Genomics England hosting: http://ukcloud.com/wp-content/uploads/2016/07/UKCloud_CaseStudy_RGB_Digital_Genomics.pdf
 * https://www.digitalmarketplace.service.gov.uk/g-cloud/services/7456481668431278
 * http://ukcloud.com/what-we-do/platform-as-a-service/digital-application-platform
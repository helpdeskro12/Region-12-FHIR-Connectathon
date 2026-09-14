
# September 2026 Philippines FHIR® Connectathon – General Santos, SOCCSKSARGEN, Philippines

 **Disclaimer:** This repository is adapted from materials and artifacts used during the **Boracay FHIR Connectathon held on June 22-26, 2026**. It has been modified for use in the **Region 12 FHIR Connectathon** and may differ from the original repository and event materials.

The September 2026 Region 12 FHIR® Connectathon is co-organized by the Department of Health Center for Health Development Region 12 with the UPM Standards and Interoperability Lab (SILab). In-kind support and funding were provided by the Strengthening Standards Capability Project (SSCP) of the Commonwealth Scientific and Industrial Research Organization (CSIRO), UP Mindanao, and other key stakeholders.

This Connectathon represents a milestone in CHD Region 12's digital health interoperability journey, bringing together healthcare systems, EMR vendors, and government agencies to advance standardized health data exchange using FHIR® profiles including PH Core, and eReferral (PeReF) specifications.

The Connectathon aims to foster interoperability across health systems by providing opportunities for healthcare system developers, business owners, vendors, government agencies, hospitals, and EMR providers to participate in critical use-case scenarios, validate emerging FHIR Implementation Guides, and build a community of practice around standards-based digital health.

## CONNECTATHON OBJECTIVES

- ### Primary Objectives
  1. **Capacity Building**: Equip IT professionals, decision-makers, and healthcare teams with foundational knowledge of interoperability standards and FHIR implementation best practices
  2. **Standards Validation**: Test and validate emerging FHIR Implementation Guides (PH Core, eReferral, and Immunization) across real-world health system use cases
  3. **Interoperability Testing**: Demonstrate data exchange and system interoperability using standardized FHIR profiles across multiple tracks
  4. **Feedback & Refinement**: Capture technical issues, gaps, and lessons learned to inform the next iteration of FHIR IGs and national interoperability standards
  5. **Governance & Scale-up**: Engage regional agencies, hospitals, LGUs, and EMR vendors in governance discussions to generate policy recommendations for national scale-up, including an integrated regional Health IT investment plan.

- ### Secondary Objectives
  1. Validate terminology mappings and workflow simulations developed using the WHO SMART Guidelines
  2. Establish a sustainable community of practice around FHIR standards in the Philippines and Region 12
  3. Provide feedback to the Department of Health on the results of the connectathon
  4. Generate evidence and documentation to support the Philippine Digital Health Strategy
     
## DISCLAIMER: 
- ***The PH Core IG and PH eReferral IG are draft versions under active development and are not intended for production use. Both guides will be refined and updated based on feedback, issues, and recommendations gathered during the June Connectathon. Content, profiles, and implementation details are subject to change.***

## Postman Collection

Participants are requested to install Postman prior to the event. Instructions are here [https://learning.postman.com/docs/getting-started/installation/install-app].

A fully parameterized Postman collection is available at [`ph-ereferral-collection/`](ph-ereferral-collection/) for testing the PH eReferral (Track 1) workflow. Import both files into Postman:

| File | Description |
|------|-------------|
| [`ph-ereferral-collection.json`](ph-ereferral-collection/ph-ereferral-collection.json) | Collection with 18 requests: 1 combined Bundle transaction (POST) and 17 individual resource requests (PUT/POST) covering all PH eReferral profiles |
| [`ph-ereferral-connectathon-environment.json`](ph-ereferral-collection/ph-ereferral-connectathon-environment.json) | Environment preset with `{{baseUrl}}` pointing to the FHIRLab eReferral server |

**Key features:**
- **87 collection variables** mapped to [PH eReferral Data Dictionary REF-IDs](https://build.fhir.org/ig/ph-ereferral-organization/ph-ereferral/en/data-dictionary.html) — edit once, apply everywhere
- **Identifier systems and values** (`philsysIdSystem`, `prcIdSystem`, `nhfrCodeSystem`, etc.) grouped at the top of the variables panel for quick submission management
- **Conditional PUT requests** use `PUT /{Resource}?identifier={system}\|{value}` pattern per Track 1 specifications
- **Bundle transaction** ready to submit all resources at once with proper internal `urn:uuid` references
- **Standalone POST requests** include `// PUT: ResourceType/{id}` placeholders — fill in actual IDs after running dependency PUTs

To use: import both files, set `{{baseUrl}}` if needed, then run the **Submit eReferral Bundle** request or step through individual requests.

## PARTICIPANT PACKETS
 - [Pre Connectathon Webinar Recording - September 10, 2026](https://drive.google.com/file/d/17CwBt6FdD9OlzchGQBeoeEhR81B1MYDj/view?usp=drive_link)
 - [eReferral data elements and UHC Referral Form]( https://drive.google.com/drive/folders/13-2Mq-gSoYumIrA6D3EpLUwo-2_4nnVq?usp=sharing)
 - [SMART on FHIR Recording]( https://drive.google.com/file/d/1vblKK6dxDOoQCEzOxoid87b0k_mZUh8t/view?usp=drive_link )


## EVENT OVERVIEW

(Click here for the Governance and Management track)

### Day 1

| Time | Agenda | Person/Team Responsible |
|------|---------|------------------------|
| 08:00 AM – 08:30 AM | Registration | CHD 12 |
| 08:30 AM – 08:40 AM | Opening Prayer<br>Philippine National Anthem<br>Introductions | Mae Fernando<br>Host |
| 08:40 AM – 08:50 AM | Opening Remarks | Garizaldy Epistola<br>Computer Maintenance Technologist III<br>Department of Health – SOCCSKSARGEN |
| 08:50 AM – 09:00 AM | Welcome Remarks | Dr. Exuperia B. Sabalberino, ND, MPH, CESE<br>Director IV<br>Department of Health – SOCCSKSARGEN<
| 09:00 AM – 09:15 AM | Ice Breaker | Mae Fernando<br>Project Manager<br>CHD 12 |
| 09:15 AM – 09:30 AM | The Aklan Health Information Exchange: the Public View | Dr. Alvin B. Marcelo<br>Asia eHealth Information Network|
| 09:30 AM – 09:40 AM | Connectathon: Global Perspective Presentation | Umer Nisar (CSIRO AEHRC) online |
| 09:40 AM – 09:50 AM | Connectathon: Boracay Perspective | Les Batay-an (TDG member) |
| 09:50 AM – 10:05 AM | Chronology of the Philippine Core Implementation Guide | Alvin Marcelo, MD<br>Founder, UPM SILab |
| 10:05 AM – 10:20 AM | Philippine eReferral (PHeRef) Project | John Lemuel Dalisay<br>Community Lead<br>PHeRef Project |
| 10:20 AM – 10:50 AM | Open Forum | **Panelists:**<br>Alvin Marcelo<br>John Lemuel Dalisay<br>Bong Epsitola<br>Les Batay-an |
| 10:50 AM – 11:05 AM | Morning Break | — |
| 11:05 AM – 11:20 AM | Overview of Connectathon: Objectives, Tracks, Set Up, and Use Cases | Alvin Marcelo |
| 11:20 AM – 11:40 AM | Basic FHIR API - Fan |
| 11:40 AM – 01:00 PM | Group Photo<br>Lunch Break | All Participants |
| 01:00 PM – 02:30 PM | Terminology Services and FHIR Terminology | Dr. Alvin Marcelo |
| 02:30 PM – 03:30 PM | Software Development | All Participants |
| 03:30 PM – 04:50 PM | Working Afternoon Break (Software Development) | All Participants |
| 04:50 PM – 05:00 PM | Wrap-up for Day 1 | Dr. Portia F. Marcelo <br>UP Colllege of Medicine |

### Day 2: Group 1 Governance and Management

| Time | Agenda | Person/Team Responsible |
|------|---------|------------------------|
| 08:00 AM – 08:30 AM | Registration | DOH-CHD12-SOCCSKSARGEN |
| 08:30 AM – 08:40 AM | Recap Day 1 | Dr Portia F. Marcelo |
| 08:40 AM – 10:30 AM | Drawing the Blueprint for the CHD12 Health Information Exchange | Dr. Alvin B. Marcelo |
| 10:30 AM – 11:15 AM | CHD12-SOCCSKSARGEN HIE RACI  | All Participants |
| 11:15 AM – 12:00 PM | Presentation of RACI | All Participants |
| 12:00 PM – 01:00 PM | Lunch Break | All Participants |
| 01:00 PM – 03:30 PM | Future State: a Generic Architecture for Regional Interoperability (client registry, facility registry, worker registry, terminology services) | Dr. Alvin B. Marcelo |
| 03:30 PM – 04:00 PM | Afternoon Break | All Participants |
| 04:00 PM – 04:30 PM | Future State: a Generic ISSP for Hospital Information System | All Participants |
| 04:30 PM – 04:50 PM | Costing of a Hospital Information System | Dr Portia F. Marcelo |
| 04:50 PM – 05:00 PM | Wrap-up and preparations for Day 3 | Dr. Alvin B. Marcelo

### Day 2 - Group 2 Technology

| Time | Agenda | Person/Team Responsible |
|------|---------|------------------------|
| 08:00 AM – 08:30 AM | Registration | DOH-CHD12-SOCCSKSARGEN |
| 08:30 AM – 08:40 AM | Recap Day 1 | Participant |
| 08:40 AM – 10:30 AM | Software Development | All Participants |
| 10:30 AM – 11:00 AM | Working Morning Break (Software Development) | All Participants |
| 11:00 AM – 12:00 PM | Software Development | All Participants |
| 12:00 PM – 01:00 PM | Lunch Break | All Participants |
| 01:00 PM – 03:30 PM | Software Development | All Participants |
| 03:30 PM – 04:00 PM | Afternoon Break | All Participants |
| 04:00 PM – 04:30 PM | Software Development (Polishing) | All Participants |
| 04:30 PM – 04:50 PM | Orientation for Show and Tell (Demonstration) | |
| 04:50 PM – 05:00 PM | Activity |

### Day 3

| Time | Agenda | Person/Team Responsible |
|------|---------|------------------------|
| 08:00 AM – 09:00 AM | Registration | DOH-CHD12-SOCCSKSARGEN |
| 09:00 AM – 09:20 AM | Recap Day 2 | John Lemuel Dalisay<br>SSCP consultant |
| 09:20 AM – 10:30 AM | Software Development (Polishing) | All Participants |
| 10:30 AM – 11:00 AM | Working Morning Break (Software Development) | All Participants |
| 11:00 AM – 12:00 PM | Preparation for Show and Tell | All Participants |
| 12:00 PM – 01:00 PM | Lunch Break | All Participants |
| 01:00 PM – 02:40 PM | Show and Tell | All Participants |
| 02:40 PM – 03:00 PM | Technical Review & Open Forum | Facilitator:  |
| 03:00 PM – 03:30 PM | Small-Group Discussion: Operational Readiness | All Participants |
| 03:30 PM – 03:45 PM | Afternoon Break | All Participants |
| 03:45 PM – 04:15 PM | Plenary Presentation and Feedback Session | **Reactors:**<br><br>(PHO)<br> (DOH KMITS)<br><br><br> (PSA)<br><br>**Facilitator:** Dr. Portia Marcelo |
| 04:15 PM – 04:30 PM | R12 Next Steps and Sustainability Road Map | Bong Epistola |
| 04:30 PM – 04:40 PM | Live Poll: Feedback |  |
| 04:40 PM – 04:50 PM | Closing Ceremony |  |
| 04:50 PM – 05:00 PM | Group Photo<br>Awarding of Certificates | Host |

## CONNECTATHON ACTIVITY DETAILS

- ### Track 1: PH eReferral IG - [Draft PH eReferral FHIR Implementation Guide (IG)](https://build.fhir.org/ig/ph-ereferral-organization/ph-ereferral/en/index.html)
  - **Objective**: Demonstrate forward referral (create, accept, reject) between healthcare provider network (HCPN) facilities using ServiceRequest and Task built on PH Core profiles, consistent with the Universal Health Care (UHC) Act and DOH Administrative Order (AO) 2020-0019 requirements.
 

    | Track Lead | Affiliation |
    |------------|-------------|
    | John Lemuel Dalisay | Community Lead, PeRef Project |
    
    #### **ACTIVITIES:**
     > 📖 **Essential Reading**: Participants must review the [PHeRef End-to-End Sample Case (Ana Reyes)](https://build.fhir.org/ig/ph-ereferral-organization/ph-ereferral/en/sample-case-ana-reyes.html) for complete bundle examples and step-by-step guidance on conditional updates.

     > **Bundle Examples**: [PHeRef Bundle Examples](https://build.fhir.org/ig/ph-ereferral-organization/ph-ereferral/en/sample-case-ana-reyes.html)

     ##### Conditional Update (PUT) Pattern
     All PUT operations in this track use **conditional update by identifier** — the server creates the resource if no matching identifier exists, otherwise updates the existing one:

     ```
     PUT /{Resource}?identifier={system}|{value}
     ```

     For Organization, use the NHFR code system:
     ```
     PUT /Organization?identifier=https://fhir.doh.gov.ph/phcore/Identifier/doh-nhfr-code|{organization_code}
     ```

     | Resource | Identifier System | Example |
     |----------|-------------------|---------|
     | Organization | `https://fhir.doh.gov.ph/phcore/Identifier/doh-nhfr-code` | `PUT /Organization?identifier=https://fhir.doh.gov.ph/phcore/Identifier/doh-nhfr-code|123456` |
     | Practitioner | `https://fhir.doh.gov.ph/phcore/Identifier/doh-prc-license-number` | `PUT /Practitioner?identifier=https://fhir.doh.gov.ph/phcore/Identifier/doh-prc-license-number|PRC-12345` |
     | Patient (PhilHealth) | `http://philhealth.gov.ph/fhir/Identifier/philhealth-id` | `PUT /Patient?identifier=http://philhealth.gov.ph/fhir/Identifier/philhealth-id|1234-567890` |
     | Patient (PhilSys) | `http://philsys.gov.ph/fhir/Identifier/philsys-id` | `PUT /Patient?identifier=http://philsys.gov.ph/fhir/Identifier/philsys-id|1234-567890-1234` |
     | ServiceRequest | Referral identifier | `PUT /ServiceRequest?identifier={referral_id}` |

     The NHFR (National Health Facility Registry) code system is bound via: [PH Core DOH NHFR Code](https://build.fhir.org/ig/UP-Manila-SILab/ph-core/en/StructureDefinition-ph-core-doh-nhfr-code.html)

    **Use Case 0: Terminology Preparation**
    Before submitting or retrieving an eReferral, retrieve and validate the value sets for each coded data element from the terminology server via `ValueSet/$expand`.

    | AC # | Data Element | Value Set | GET URL |
    |------|-------------|-----------|---------|
    | 0.01 | Practitioner Role | `practitioner-role` | `GET [base]/ValueSet/$expand?url=https://www.fhir.doh.gov.ph/pheref/ValueSet/practitioner-role` |
    | 0.02 | Referral Category | `referral-category` | `GET [base]/ValueSet/$expand?url=https://www.fhir.doh.gov.ph/pheref/ValueSet/referral-category` |
    | 0.03 | Reason for Referral (Service Type) | `reason-for-referral-service-type` | `GET [base]/ValueSet/$expand?url=https://www.fhir.doh.gov.ph/pheref/ValueSet/reason-for-referral-service-type` |
    | 0.04 | PWD Disability Type | `pwd-disability-type-vs` | `GET [base]/ValueSet/$expand?url=https://fhir.doh.gov.ph/pheref/ValueSet/pwd-disability-type-vs` |
    | 0.05 | Administrative Gender | `administrative-gender` (base FHIR) | `GET [base]/ValueSet/$expand?url=http://hl7.org/fhir/ValueSet/administrative-gender` |
    | 0.06 | Task Status | `task-status` (base FHIR) | `GET [base]/ValueSet/$expand?url=http://hl7.org/fhir/ValueSet/task-status` |
    | 0.07 | Contact Point System / Use | `contact-point-system` / `contact-point-use` (base FHIR) | `GET [base]/ValueSet/$expand?url=http://hl7.org/fhir/ValueSet/contact-point-system` |

    **Use Case 1: Initiating Facility Submits eReferral (PUT/POST)**
    The referring (initiating) facility submits one eReferral transaction (bundle) to the Shared Health Records (SHR). Demographics and referral metadata are PUT (using conditional update by identifier); clinical data are POST.

    | AC # | Interaction | Data Element | FHIR Resource & Element |
    |------|------------|-------------|------------------------|
    | 1.01 | PUT | Name of Referring Practitioner | `Practitioner.name` |
    | 1.02 | PUT | Care Navigator | `Practitioner.name` |
    | 1.03 | PUT | Practitioner Role | `PractitionerRole.code` |
    | 1.04 | PUT | Date & Time of Signature | `Provenance.recorded` |
    | 1.05 | PUT | Professional Signature | `Provenance.signature` |
    | 1.06 | PUT | Initiating Facility Name | `Organization.name` |
    | 1.07 | PUT | Initiating Facility NHFR Code | `Organization.identifier(NHFR).value` |
    | 1.08 | PUT | Initiating Facility Address | `Organization.address` |
    | 1.09 | PUT | Initiating Facility Contact Number | `Organization.telecom` |
    | 1.10 | PUT | Receiving Facility Name | `Organization.name` |
    | 1.11 | PUT | Receiving Facility NHFR Code | `Organization.identifier(NHFR).value` |
    | 1.12 | PUT | HCPN Name | `Organization.identifier(HCPN).value` |
    | 1.13 | PUT | Date of Referral | `ServiceRequest.authoredOn` |
    | 1.14 | PUT | Referral Category | `ServiceRequest.priority` |
    | 1.15 | PUT | Reason for Referral (service type) | `ServiceRequest.category` |
    | 1.16 | PUT | Time Called | `Task.authoredOn` |
    | 1.17 | PUT | Action Point: Received | `Task.status` |
    | 1.18 | PUT | Action Point: Referred (Forwarded) | `Task.status` |
    | 1.19 | PUT | Patient Full Name | `Patient.name` |
    | 1.20 | PUT | Sex (Administrative Gender) | `Patient.gender` |
    | 1.21 | PUT | Birth Date | `Patient.birthDate` |
    | 1.22 | PUT | Age (computed) | `Patient.birthDate` |
    | 1.23 | PUT | Identity Number (PhilSys) | `Patient.identifier(PHCorePhilSysID)` |
    | 1.24 | PUT | PhilHealth ID | `Patient.identifier(PHCorePhilHealthID)` |
    | 1.25 | PUT | Patient Address | `Patient.address` |
    | 1.26 | PUT | Contact Number | `Patient.telecom` |
    | 1.27 | PUT | Accompanied By / Next of Kin | `Patient.contact` |
    | 1.28 | PUT | Patient Disability Registration | `Patient.extension[pwdDisability]` |
    | 1.29 | POST | Chief Complaint | `Condition.code.text`, `Condition.category = problem-list-item` |
    | 1.30 | POST | Clinical History | `Condition.note` |
    | 1.31 | POST | Working Impression (clinical reason) | `Condition.code`, `Condition.category = encounter-diagnosis` |
    | 1.32 | POST | Vital Signs – Blood Pressure | `Observation` (code, value[x], category=vital-signs, component systolic/diastolic) |
    | 1.33 | POST | Vital Signs – Heart Rate | `Observation` (code, value[x], category=vital-signs) |
    | 1.34 | POST | Vital Signs – Respiratory Rate | `Observation` (code, value[x], category=vital-signs) |
    | 1.35 | POST | Vital Signs – Oxygen Saturation | `Observation` (code, value[x], category=vital-signs) |
    | 1.36 | POST | Vital Signs – Temperature | `Observation` (code, value[x], category=vital-signs) |
    | 1.37 | POST | Vital Signs – Weight | `Observation` (code, value[x], category=vital-signs) |
    | 1.38 | POST | Treatment Given | `Procedure.note` |
    | 1.39 | POST | Laboratory Results (attachments) | `DiagnosticReport.presentedForm(Attachment.data)` |

    **Use Case 2: Receiving Facility Retrieves eReferral (GET)**
    The receiving facility retrieves the eReferral transaction (bundle) from the SHR previously submitted by the referring facility and updates action points.

    | AC # | Interaction | Data Element | FHIR Resource & Element |
    |------|------------|-------------|------------------------|
    | 2.01 | GET | Name of Referring Practitioner | `Practitioner.name` |
    | 2.02 | GET | Care Navigator | `Practitioner.name` |
    | 2.03 | GET | Practitioner Role | `PractitionerRole.code` |
    | 2.04 | GET | Date & Time of Signature | `Provenance.recorded` |
    | 2.05 | GET | Professional Signature | `Provenance.signature` |
    | 2.06 | GET | Initiating Facility Name | `Organization.name` |
    | 2.07 | GET | Initiating Facility NHFR Code | `Organization.identifier(NHFR).value` |
    | 2.08 | GET | Initiating Facility Address | `Organization.address` |
    | 2.09 | GET | Initiating Facility Contact Number | `Organization.telecom` |
    | 2.10 | GET | Receiving Facility Name | `Organization.name` |
    | 2.11 | GET | Receiving Facility NHFR Code | `Organization.identifier(NHFR).value` |
    | 2.12 | GET | HCPN Name | `Organization.identifier(HCPN).value` |
    | 2.13 | GET | Date of Referral | `ServiceRequest.authoredOn` |
    | 2.14 | GET | Referral Category | `ServiceRequest.priority` |
    | 2.15 | GET | Reason for Referral (service type) | `ServiceRequest.category` |
    | 2.16 | GET | Time Called | `Task.authoredOn` |
    | 2.17 | PUT | Action Point: Received | `Task.status` |
    | 2.18 | PUT | Action Point: Referred (Forwarded) | `Task.status` |
    | 2.19 | GET | Patient Full Name | `Patient.name` |
    | 2.20 | GET | Sex (Administrative Gender) | `Patient.gender` |
    | 2.21 | GET | Birth Date | `Patient.birthDate` |
    | 2.22 | GET | Age (computed) | `Patient.birthDate` |
    | 2.23 | GET | Identity Number (PhilSys) | `Patient.identifier(PHCorePhilSysID)` |
    | 2.24 | GET | PhilHealth ID | `Patient.identifier(PHCorePhilHealthID)` |
    | 2.25 | GET | Patient Address | `Patient.address` |
    | 2.26 | GET | Contact Number | `Patient.telecom` |
    | 2.27 | GET | Accompanied By / Next of Kin | `Patient.contact` |
    | 2.28 | GET | Patient Disability Registration | `Patient.extension[pwdDisability]` |
    | 2.29 | GET | Chief Complaint | `Condition.code.text`, `Condition.category = problem-list-item` |
    | 2.30 | GET | Clinical History | `Condition.note` |
    | 2.31 | GET | Working Impression (clinical reason) | `Condition.code`, `Condition.category = encounter-diagnosis` |
    | 2.32 | GET | Vital Signs – Blood Pressure | `Observation` (code, value[x], category=vital-signs, component) |
    | 2.33 | GET | Vital Signs – Heart Rate | `Observation` (code, value[x], category=vital-signs) |
    | 2.34 | GET | Vital Signs – Respiratory Rate | `Observation` (code, value[x], category=vital-signs) |
    | 2.35 | GET | Vital Signs – Oxygen Saturation | `Observation` (code, value[x], category=vital-signs) |
    | 2.36 | GET | Vital Signs – Temperature | `Observation` (code, value[x], category=vital-signs) |
    | 2.37 | GET | Vital Signs – Weight | `Observation` (code, value[x], category=vital-signs) |
    | 2.38 | GET | Treatment Given | `Procedure.note` |
    | 2.39 | GET | Laboratory Results (attachments) | `DiagnosticReport.presentedForm(Attachment.data)` |

    **Activity 4: LGU Dashboard (PHO Only) — Read-Only Reporting**
    - Search patients seen by facility based on Referral Category and Reason for Referral (GET) → 200 OK – returns list
    - Generate report based on Referral Category and Reason for Referral (GET) → 200 OK – returns report



- ### Track 2: PH Core IG - [Draft PH Core FHIR Implementation Guide (IG)](https://build.fhir.org/ig/UP-Manila-SILab/ph-core/en/index.html)
  - **Objective**: Validate that PH Core IG v0.2.0 profiles are implementable by creating, exchanging, and validating a complete encounter record — using the Encounter profile (primary) with Patient, Organization, Condition, Observation, Practitioner, and optionally PractitionerRole — including Philippines-specific identifiers, extensions, and terminology bindings.


    | Track Lead | Affiliation |
    |------------|-------------|
    | Name | Interoperability Specialist |
    | Name | Director III |


     #### **ACTIVITIES:**
      > **Bundle Example**: [bundle-acs-case-example](https://build.fhir.org/ig/UP-Manila-SILab/ph-core/en/Bundle-bundle-acs-case-example.html)

    1. **Create Encounter Record — Submit resources to FHIRLab**
       - POST /Patient — create patient with PH Core identifiers (PhilSys, PhilHealth, NHFR)
       - POST /Organization — create facility organization
       - POST /Practitioner — create attending practitioner
       - POST /PractitionerRole — associate practitioner with organization and role
       - POST /Condition — add encounter diagnosis (category = encounter-diagnosis)
       - POST /Observation — add vital signs (blood pressure, heart rate, temperature, etc.) with category = vital-signs
       - POST /Encounter — create the encounter referencing Patient, Practitioner, Organization, and Condition
       - Validate each resource against the PH Core IG profiles

    2. **Search and Retrieve — Query records from FHIRLab**
       - GET /Patient?identifier=... — search patient by PhilSys or PhilHealth ID
       - GET /Encounter?patient=... — retrieve encounter history for a patient
       - GET /Observation?patient=...&category=vital-signs — retrieve vital signs
       - GET /Condition?patient=... — retrieve conditions/diagnoses
       - GET /Organization — retrieve facility details
       - Verify returned resources conform to PH Core profiles

    3. **Bundle Transaction — Submit multiple resources in a single transaction**
       - POST with Bundle.type = transaction containing Patient, Organization, Practitioner, PractitionerRole, Encounter, Condition, and Observation entries
       - Verify full transaction succeeds (200 OK) or fails atomically (4xx/5xx)
       - Retrieve the bundle entries using the returned references





## FHIR SERVERS AVAILABLE FOR TESTING DURING THE CONNECTATHON

| Version | Server | Endpoint | Capabilities |
|-------------|---------|-------------|-------------|
| FHIR R4 | FHIRLab (HAPI FHIR) - PH eReferral | [cdr.pheref.fhirlab.net](https://cdr.pheref.fhirlab.net/) | CRUD, transaction, validation |
| FHIR R4 | FHIRLab (HAPI FHIR) - PH Core | [cdr.phcore.fhirlab.net](https://cdr.phcore.fhirlab.net/) | CRUD, transaction, validation |
| FHIR R4 | Ontoserver Terminology | [ontoserver.csiro.au/ui/about](https://ontoserver.csiro.au/ui/about) | $expand, $validate-code, $lookup |
| FHIR R4 | Ontoserver with Shrimp Viewer | [ontoserver.csiro.au/shrimp/](https://ontoserver.csiro.au/shrimp/?concept=138875005&valueset=http%3A%2F%2Fsnomed.info%2Fsct%3Ffhir_vs&fhir=https%3A%2F%2Ftx.fhirlab.net%2Ffhir) | Terminology browsing & visualization |
| FHIR R4 | FHIRPortal (HAPI FHIR) | To be updated | Back Up HAPI FHIR Server. **Do not use unless instructed**|

> **Note**: FHIRLab is an open interoperability sandbox maintained as part of The Strengthening Standards Capability Project (SSCP), co-funded by CSIRO Australia and the Australian Government, Department of Foreign Affairs and Trade. FHIR servers will remain accessible for testing and ongoing learning activities post-Connectathon.


## INTERNATIONAL SYNTACTIC AND SEMANTIC STANDARDS

**Participants should familiarize themselves with the following foundational standards:**

  - **[HL7 FHIR](https://www.fhir.org/)** (Fast Healthcare Interoperability Resources)
    - FHIR R4 standard resources and REST API conventions
    - Profile definition and implementation guidance
    - How to submit FHIR resources with Profiles from a FHIR Implementation Guide
    - How to retrieve and expand ValueSets
  
    > Note: FHIR R4 is aligned with national digital health initiatives in the Philippines.

  - **[OpenHIE Architecture](https://ohie.org/architecture-specification/)** - Digital health system reference architecture

  - **[SNOMED CT](https://www.snomed.org/what-is-snomed-ct)** - Clinical terminology standard

  - **[ICD-10](https://icd.who.int/browse10/2019/en)** - International disease classification

  - **[LOINC](https://loinc.org/)** - Laboratory and clinical observation codes

  - **[WHO SMART Guidelines](https://www.who.int/teams/digital-health-and-innovation/smart-guidelines)** - Standards-based workflow approach


## FHIRLab TOOLS AND RESOURCES

- ### FHIR Servers and Tooling
  - **[FHIR Server — PH eReferral (HAPI FHIR)](https://cdr.pheref.fhirlab.net/fhir)** - eReferral FHIR server for resource submissions and retrieval
  - **[FHIR Server — PH Core (HAPI FHIR)](https://cdr.phcore.fhirlab.net/fhir)** - PH Core FHIR server for resource submissions and retrieval
  - **[Terminology Server (Ontoserver Endpoint)](https://tx.fhirlab.net/fhir)** - ValueSet and terminology operations
  - **[Terminology Browser (Ontoserver + Shrimp)](https://ontoserver.csiro.au/shrimp/)** - Visual terminology browsing and mapping

- ### Local Testing Tools (Optional)
  - **[FHIR CLI](https://hapifhir.io/hapi-fhir/docs/tools/hapi_fhir_cli.html#server-run-server)** - Run a local HAPI FHIR server for testing
  - **[FHIR Validator](https://validator.fhirlab.net)** - Online resource validation against FHIR IGs
  - **[Postman](https://www.postman.com/)** - API testing and development tool
  - **[UploadFIG Utility](https://github.com/brianpos/UploadFIG)** - Upload custom FHIR IGs to local servers
    
> Note: FHIR® Lab is part of The Strengthening Standards Capability Project (SSCP), co-funded by CSIRO Australia and Australian Government, Department of Foreign Affairs and Trade.


## CONNECTATHON SUCCESS CRITERIA

**Participants will demonstrate success through the following activities:**

1. ✅ Validate FHIR resources against the draft PH Core and eReferral Implementation Guides
2. ✅ Successfully submit individual FHIR resources to the test FHIR server
3. ✅ Successfully submit FHIR bundles containing related resources in a single transaction
4. ✅ Perform FHIR search queries using standard search parameters
5. ✅ Retrieve resources using patient identifiers and clinical filters
6. ✅ Verify content accuracy and completeness of exchanged data
7. ✅ Provide structured feedback on gaps, issues, and recommendations for profile refinement
8. ✅ Document lessons learned and best practices for implementation


## HOW TO PREPARE FOR THE CONNECTATHON?

1. **Review the FHIR IGs**: Familiarize yourself with the PH Core and eReferral Implementation Guides
2. **Understand FHIR Basics**: Review HL7 FHIR fundamentals and REST API conventions
3. **Set Up Access**: Ensure you have access to the FHIRLab servers (no credentials required)
4. **Download Tools**: Install Postman and review the prepared collections and sample data
5. **Test Locally**: Use the sample Postman requests to test against the FHIRLab servers
6. **Bring Questions**: Come prepared with questions about implementation challenges or unclear specifications

## SUPPLEMENTARY INFORMATION

### Additional Resources

- [Participant Packet](https://drive.google.com/drive/folders/13-2Mq-gSoYumIrA6D3EpLUwo-2_4nnVq?usp=drive_link)
- [PHeRef End-to-End Sample Case (Ana Reyes)](https://build.fhir.org/ig/ph-ereferral-organization/ph-ereferral/en/sample-case-ana-reyes.html) — Reference bundle examples and conditional update guide for Track 1
- [FHIR Official Documentation](https://www.fhir.org/summary.html)
- [HL7 FHIR Community Chat](https://chat.fhir.org/)
- [Philippine eHealth Roadmap](https://doh.gov.ph/)
- [NTHC Publications and Resources](https://nthc.upmanila.edu.ph/)

### Feedback and Reporting

Participants are encouraged to submit structured feedback on:

- **Profile Conformance**: Gaps or inconsistencies in the FHIR profiles
- **Terminology Mappings**: Issues with local code mappings
- **Server Responses**: Technical issues or unexpected behavior
- **Implementation Challenges**: Real-world barriers to adoption
- **Best Practices**: Recommendations for streamlined implementation

👉 [FHIR IG Technical Feedback Sheet](https://docs.google.com/spreadsheets/d/1WU8-8s-SLfpmF04wGHurtX7mRZnqGI2dcPfHgsN7LxA/edit?usp=sharing)

---

## Disclaimer

FHIR® is a registered trademark of Health Level Seven International.

This Connectathon is made possible through the collaborative efforts of the Department of Health (DOH) Center for Health Development 12.

For questions and queries regarding the Connectathon, please contact **ict@ro12.doh.gov.ph**.

---


**Last Updated**: June 23, 2026  
**Next Review**: Post-Connectathon Debrief

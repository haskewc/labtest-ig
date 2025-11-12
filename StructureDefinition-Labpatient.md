# Example Patient Profile - Zimbabwe Test IG v0.1.0

* [**Table of Contents**](toc.md)
* [**Indices**](indices.md)
* [**Artifact Index**](artifacts.md)
* **Example Patient Profile**

## Resource Profile: Example Patient Profile 

| | |
| :--- | :--- |
| *Official URL*:http://smart.who.int/ig-empty/StructureDefinition/Labpatient | *Version*:0.1.0 |
| Draft as of 2025-11-12 | *Computable Name*:Labpatient |

 
Example of a profile of Patient 

**Usages:**

* This Profile is not used by any profiles in this Implementation Guide

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/smart.who.int.ig-empty|current/StructureDefinition/Labpatient)

### Formal Views of Profile Content

 [Description of Profiles, Differentials, Snapshots and how the different presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-Labpatient.csv), [Excel](StructureDefinition-Labpatient.xlsx), [Schematron](StructureDefinition-Labpatient.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "Labpatient",
  "url" : "http://smart.who.int/ig-empty/StructureDefinition/Labpatient",
  "version" : "0.1.0",
  "name" : "Labpatient",
  "title" : "Example Patient Profile",
  "status" : "draft",
  "date" : "2025-11-12T08:09:53+00:00",
  "publisher" : "MoHKI",
  "contact" : [
    {
      "name" : "MoHKI",
      "telecom" : [
        {
          "system" : "url",
          "value" : "http://kiribati.gov.ki"
        }
      ]
    }
  ],
  "description" : "Example of a profile of Patient",
  "jurisdiction" : [
    {
      "coding" : [
        {
          "system" : "http://unstats.un.org/unsd/methods/m49/m49.htm",
          "code" : "296",
          "display" : "Kiribati"
        }
      ]
    }
  ],
  "fhirVersion" : "4.0.1",
  "mapping" : [
    {
      "identity" : "rim",
      "uri" : "http://hl7.org/v3",
      "name" : "RIM Mapping"
    },
    {
      "identity" : "cda",
      "uri" : "http://hl7.org/v3/cda",
      "name" : "CDA (R2)"
    },
    {
      "identity" : "w5",
      "uri" : "http://hl7.org/fhir/fivews",
      "name" : "FiveWs Pattern Mapping"
    },
    {
      "identity" : "v2",
      "uri" : "http://hl7.org/v2",
      "name" : "HL7 v2 Mapping"
    },
    {
      "identity" : "loinc",
      "uri" : "http://loinc.org",
      "name" : "LOINC code for the element"
    }
  ],
  "kind" : "resource",
  "abstract" : false,
  "type" : "Patient",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/Patient",
  "derivation" : "constraint",
  "differential" : {
    "element" : [
      {
        "id" : "Patient",
        "path" : "Patient"
      },
      {
        "id" : "Patient.name",
        "path" : "Patient.name",
        "short" : "Official name (i.e., legal name) of patient",
        "definition" : "Official name (i.e., legal name) of the patient, corresponding to `official` in [this value set](https://www.hl7.org/fhir/valueset-name-use.html).",
        "min" : 1,
        "max" : "1"
      },
      {
        "id" : "Patient.name.family",
        "path" : "Patient.name.family",
        "short" : "Patient's last name",
        "min" : 1
      },
      {
        "id" : "Patient.name.given",
        "path" : "Patient.name.given",
        "short" : "Patient's first name",
        "min" : 1,
        "max" : "1"
      },
      {
        "id" : "Patient.gender",
        "path" : "Patient.gender",
        "min" : 1,
        "binding" : {
          "strength" : "required",
          "valueSet" : "http://smart.who.int/ig-empty/ValueSet/ZimGenderVS"
        }
      },
      {
        "id" : "Patient.birthDate",
        "path" : "Patient.birthDate",
        "comment" : "If exact date of birth is partially or completely unknown, Implementers SHALL populate this element with the date of birth information listed on the patient's government-issued identification."
      },
      {
        "id" : "Patient.deceased[x]",
        "path" : "Patient.deceased[x]",
        "type" : [
          {
            "code" : "dateTime"
          }
        ]
      },
      {
        "id" : "Patient.maritalStatus",
        "path" : "Patient.maritalStatus",
        "binding" : {
          "strength" : "required",
          "valueSet" : "http://hl7.org/fhir/ValueSet/marital-status"
        }
      }
    ]
  }
}

```

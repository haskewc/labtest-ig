# Zimbabwe Gender Value Set - Zimbabwe Test IG v0.1.0

* [**Table of Contents**](toc.md)
* [**Indices**](indices.md)
* [**Artifact Index**](artifacts.md)
* **Zimbabwe Gender Value Set**

## ValueSet: Zimbabwe Gender Value Set 

| | |
| :--- | :--- |
| *Official URL*:http://smart.who.int/ig-empty/ValueSet/ZimGenderVS | *Version*:0.1.0 |
| Draft as of 2025-11-12 | *Computable Name*:ZimGenderVS |

 
Administrative Gender 

 **References** 

* [Example Patient Profile](StructureDefinition-Labpatient.md)

### Logical Definition (CLD)

 

### Expansion

-------

 Explanation of the columns that may appear on this page: 

| | |
| :--- | :--- |
| Level | A few code lists that FHIR defines are hierarchical - each code is assigned a level. In this scheme, some codes are under other codes, and imply that the code they are under also applies |
| System | The source of the definition of the code (when the value set draws in codes defined elsewhere) |
| Code | The code (used as the code in the resource instance) |
| Display | The display (used in the*display*element of a[Coding](http://hl7.org/fhir/R4/datatypes.html#Coding)). If there is no display, implementers should not simply display the code, but map the concept into their application |
| Definition | An explanation of the meaning of the concept |
| Comments | Additional notes about how to use the code |



## Resource Content

```json
{
  "resourceType" : "ValueSet",
  "id" : "ZimGenderVS",
  "url" : "http://smart.who.int/ig-empty/ValueSet/ZimGenderVS",
  "version" : "0.1.0",
  "name" : "ZimGenderVS",
  "title" : "Zimbabwe Gender Value Set",
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
  "description" : "Administrative Gender",
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
  "compose" : {
    "include" : [
      {
        "system" : "http://hl7.org/fhir/administrative-gender",
        "concept" : [
          {
            "code" : "male",
            "display" : "Blue"
          },
          {
            "code" : "female",
            "display" : "Pink"
          },
          {
            "code" : "unknown",
            "display" : "Not determined"
          }
        ]
      }
    ]
  }
}

```

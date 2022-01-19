# Medication Card document

In a primary system, different medications are documented in a treatment context. Primary systems can use this Exchange Format to generate a Medication Card document with the help of the Content Creator.

## Composite

In the resource "Composition", general information about the document is specified

* *id:* Local id of the resource (line 3)
* *language:* Specifies the language of the document (line 4)
* *text:* Presents the narrative text of the resource (line 5 to 8)
* *extension:* Extensions used (line 9 to 16)
* *identifier:* A version-independent identifier for the Composition (line 17 to 20)
* *status:* The status of the document (line 21)
* *type:* Specifies the particular kind of composition (line 22 to 35)

```
  1 "resource": {
  2        "resourceType": "Composition",
  3        "id": "2-7-MedicationCard",
  4        "language": "de-CH",
  5        "text": {
  6          "status": "extensions",
  7          "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\" xml:lang=\"de-CH\" lang=\"de-CH\"><p><b>Generated Narrative</b></p><p><b>EPR Information Recipient</b>: <a href=\"#Patient_MonikaWegmuellerRecipient\">See above (Patient/MonikaWegmuellerRecipient)</a></p><p><b>identifier</b>: id: urn:uuid:6b6ed376-a7da-44cb-92d1-e75ce1ae73b0</p><p><b>status</b>: final</p><p><b>type</b>: <span title=\"Codes: {http://loinc.org 56445-0}, {http://snomed.info/sct 721912009}\">Medication summary</span></p><p><b>date</b>: Feb 4, 2012, 2:05:00 PM</p><p><b>author</b>: </p><ul><li><a href=\"#Practitioner_FamilienHausarzt\">See above (Practitioner/FamilienHausarzt)</a></li><li><a href=\"#Organization_Hausarzt\">See above (Organization/Hausarzt)</a></li></ul><p><b>title</b>: Medikationsplan</p><p><b>confidentiality</b>: N</p><p><b>custodian</b>: <a href=\"#Organization_Custodian\">See above (Organization/Custodian)</a></p></div>"
  8        },
  9        "extension": [
 10          {
 11            "url": "http://fhir.ch/ig/ch-core/StructureDefinition/ch-ext-epr-informationrecipient",
 12            "valueReference": {
 13              "reference": "Patient/MonikaWegmuellerRecipient"
 14            }
 15          }
 16        ],
 17        "identifier": {
 18          "system": "urn:ietf:rfc:3986",
 19          "value": "urn:uuid:6b6ed376-a7da-44cb-92d1-e75ce1ae73b0"
 20        },
 21        "status": "final",
 22        "type": {
 23          "coding": [
 24            {
 25              "system": "http://loinc.org",
 26              "code": "56445-0",
 27              "display": "Medication summary"
 28            },
 29            {
 30              "system": "http://snomed.info/sct",
 31              "code": "721912009",
 32              "display": "Medication summary document (record artifact)"
 33            }
 34          ]
 35        }, 
```

* *subject:* Who or what the composition is about (line 36 to 41)
* *date:* The composition editing time (line 39)
* *author:* Identifies who is responsible for the information in the composition (line 40 to 53)
```
 36 "subject": {
 37          "reference": "Patient/MonikaWegmueller"
 38        },
 39        "date": "2012-02-04T14:05:00+01:00",
 40        "author": [
 41          {
 42            "extension": [
 43              {
 44                "url": "http://fhir.ch/ig/ch-core/StructureDefinition/ch-ext-epr-time",
 45                "valueDateTime": "2012-02-04T13:55:00+01:00"
 46              }
 47            ],
 48            "reference": "Practitioner/FamilienHausarzt"
 49          },
 50          {
 51            "reference": "Organization/Hausarzt"
 52          }
 53        ],
```
* *title:* Human readable label for the composite
```
54        "title": "Medikationsplan",
```
* *confidentiality:* Level of confidentiality of the Composition
```
 55        "confidentiality": "N",
 56        "_confidentiality": {
 57          "extension": [
 58            {
 59              "url": "http://fhir.ch/ig/ch-core/StructureDefinition/ch-ext-epr-confidentialitycode",
 60              "valueCodeableConcept": {
 61                "coding": [
 62                  {
 63                    "system": "http://snomed.info/sct",
 64                    "code": "17621005",
 65                    "display": "Normally accessible"
 66                  }
 67                ]
 68              }
 69            }
 70          ]
 71        },
```
* *custodian:* Organization who is responsible for the document and access
```
 72        "custodian": {
 73          "reference": "Organization/Custodian"
 74        },
```
* *section:* The root of the sections that make up the composition.
```
 75        "section": [
 76          {
 77            "title": "Medikamentenliste",
 78            "code": {
 79              "coding": [
 80                {
 81                  "system": "http://loinc.org",
 82                  "code": "10160-0",
 83                  "display": "History of medication use"
 84                }
 85              ]
 86            },
 87            "entry": [
 88              {
 89                "reference": "MedicationStatement/2-7-MedStatBeloczok"
 90              },
 91              {
 92                "reference": "MedicationStatement/2-7-MedStatNorvasc"
 93              }
 94            ]
 95          },
 96          {
 97            "title": "Kommentar",
 98            "code": {
 99              "coding": [
100                {
101                  "system": "http://loinc.org",
102                  "code": "48767-8",
103                  "display": "Annotation comment"
104                }
105              ]
106            },
107            "text": {
108              "status": "generated",
109              "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\">\n              <span id=\"co1\">\n                  Kommentar zu Medication Treatment\n              </span>\n            </div>"
110            }
111          },
112          {
113            "title": "Original Darstellung",
114            "code": {
115              "coding": [
116                {
117                  "system": "http://loinc.org",
118                  "code": "55108-5",
119                  "display": "Clinical presentation"
120                }
121              ]
122            },
123            "text": {
124              "status": "generated",
125              "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\">\n              <a href=\"Binary/2-7-pdf\">Representation of the original view</a>\n            </div>"
126            },
127            "entry": [
130              {
131                "reference": "Binary/2-7-pdf"
132              }
133            ]
134          }
135        ]
136      }
137    },
```

## Information about the patient

In the "Patient" resource, the demographic and administrative data of a patient are specified.

```
  "resource": {
        "resourceType": "Patient",
        "id": "MonikaWegmueller",
        "text": {
          "status": "generated",
          "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\"><p><b>Generated Narrative</b></p><p><b>identifier</b>: Medical record number: 11111111</p><p><b>name</b>: Monika Wegmüller </p><p><b>gender</b>: female</p><p><b>birthDate</b>: 1943-05-15</p><p><b>address</b>: Wiesenstr. 12 Zürich 8003 CH </p></div>"
        },
        "identifier": [
          {
            "type": {
              "coding": [
                {
                  "system": "http://terminology.hl7.org/CodeSystem/v2-0203",
                  "code": "MR"
                }
              ]
            },
            "system": "urn:oid:2.999",
            "value": "11111111"
          }
        ],
        "name": [
          {
            "family": "Wegmüller",
            "given": [
              "Monika"
            ]
          }
        ],
        "gender": "female",
        "birthDate": "1943-05-15",
        "address": [
          {
            "line": [
              "Wiesenstr. 12"
            ],
            "city": "Zürich",
            "postalCode": "8003",
            "country": "CH"
          }
        ]
      }
    },
```

## Information about the practitioner

The resource Practionier indicates which Practionier has prescribed a medication

```
  1 "resource": {
  2                "resourceType": "Practitioner",
  3                "id": "c23e26e7-cbb9-4155-9117-ae31163c833f",
  4                "identifier": [{
  5                        "system": "urn:oid:2.51.1.3",
  6                        "value": "7601003180268"
  7                    }
  8                ],
  9                "name": [{
 10                        "family": "Crausaz",
 11                        "given": ["Christophe"]
 12                    }
 13                ]
 14            }
```

## Information about the organization

The resource stores the information about the organization that create the Medication Card document

```
  1 "resource": {
  2                "resourceType": "Organization",
  3                "id": "dc0dead8-eefc-4b94-9a6d-01e521db765c",
  4                "identifier": [{
  5                        "system": "urn:oid:2.51.1.3",
  6                        "value": "7601001362383"
  7                    }
  8                ],
  9                "name": "HCI Solutions AG",
 10                "address": [{
 11                       "line": ["Untermattweg 8"],
 12                        "city": "Bern 1",
 13                        "postalCode": "3000",
 14                        "country": "CH"
 15                    }
 16                ]
 17            }
```

## Medication

In the following resource "MedicationStatement" the data of the patient's medication are specified

### Medication information
* *id:* Local id of the resource (line 2)
* *text:* Presents the narrative text of the resource (line 3, 19, 54)
* *contained:* These resources do not have an independent existence apart from the resource that contains them (line 7 to 73)
* *code:* A code (or set of codes) that specify this medication, or a textual description if no code is available. (line 11, 25, 35, 41, 50, 67)
* *coding* A reference to a code defined by a terminology system. (line 12,22, 47)
* *form* Describes the form of the medication. Powder; tablets; capsule. (line 21 to 29)
* *amount:* A relationship of two Quantity values - expressed as a numerator and a denominator. (line 30 to 36)
* *ingredient:*  Particular ingredient of a medication (line 44 to 71)
* *strength:* A relationship of two Quantity values - expressed as a numerator and a denominator (line 56 to 69)





```
  1 "resourceType": "MedicationStatement",
  2        "id": "2-7-MedStatBeloczok",
  3        "text": {
  4          "status": "extensions",
  5          "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\"><p><b>Generated Narrative</b></p><blockquote><p><b>CH EMED Extension Treatment Plan</b></p><h3>Urls</h3><table class=\"grid\"><tr><td>-</td></tr><tr><td>*</td></tr></table><p><b>value</b>: id: urn:uuid:5712fffe-20c6-11e6-b67b-9e71128cae77</p><h3>Urls</h3><table class=\"grid\"><tr><td>-</td></tr><tr><td>*</td></tr></table><p><b>value</b>: id: urn:uuid:5712fffe-20c6-11e6-b67b-9e71128cae77</p></blockquote><p><b>identifier</b>: id: urn:uuid:d0f885ca-afa6-4e7e-905d-f7698f9607aa</p><p><b>status</b>: completed</p><p><b>medication</b>: <a name=\"med\"> </a></p><blockquote><p><b>code</b>: <span title=\"Codes: {urn:oid:2.51.1.1 7680521101306}\">BELOC ZOK Ret Tabl 50 mg</span></p><p><b>form</b>: <span title=\"Codes: {urn:oid:0.4.0.127.0.16.1.1.2.1 10219000}\">Tablet</span></p><p><b>amount</b>: 30 Tablet (unit of presentation)/1 Package</p><h3>Ingredients</h3><table class=\"grid\"><tr><td>-</td><td><b>Item[x]</b></td><td><b>Strength</b></td></tr><tr><td>*</td><td><span title=\"Codes: {http://snomed.info/sct 372826007}\">Metoprolol</span></td><td>50 milligram/1 Tablet (unit of presentation)</td></tr></table></blockquote><p><b>subject</b>: <a href=\"#Patient_MonikaWegmueller\">See above (Patient/MonikaWegmueller)</a></p><p><b>reasonCode</b>: <span title=\"Codes: \">Bluthochdruck</span></p><p><b>note</b>: -</p><h3>Dosages</h3><table class=\"grid\"><tr><td>-</td></tr><tr><td>*</td></tr><tr><td>*</td></tr><tr><td>*</td></tr></table></div>"
  6        },
  7        "contained": [
  8          {
  9            "resourceType": "Medication",
 10            "id": "med",
 11            "code": {
 12              "coding": [
 13                {
 14                  "system": "urn:oid:2.51.1.1",
 15                  "code": "7680521101306",
 16                "display": "BELOC ZOK Ret Tabl 50 mg 30 Stk"
 17              }
 18            ],
 19            "text": "BELOC ZOK Ret Tabl 50 mg"
 20          },
 21          "form": {
 22            "coding": [
 23              {
 24                "system": "urn:oid:0.4.0.127.0.16.1.1.2.1",
 25                "code": "10219000",
 26                "display": "Tablet"
 27              }
 28            ]
 29          },
 30          "amount": {
 31            "numerator": {
 32              "value": 30,
 33              "unit": "Tablet (unit of presentation)",
 34              "system": "http://snomed.info/sct",
 35              "code": "732936001"
 36            },
 37            "denominator": {
 38              "value": 1,
 39              "unit": "Package",
 40              "system": "http://unitsofmeasure.org",
 41              "code": "{Package}"
 42              }
 43            },
 44            "ingredient": [
 45              {
 46                "itemCodeableConcept": {
 47                  "coding": [
 48                    {
 49                      "system": "http://snomed.info/sct",
 50                      "code": "372826007",
 51                      "display": "Metoprolol (substance)"
 52                    }
 53                  ],
 54                  "text": "Metoprolol"
 55                },
 56                "strength": {
 57                  "numerator": {
 58                    "value": 50,
 59                    "unit": "milligram",
 60                    "system": "http://unitsofmeasure.org",
 61                    "code": "mg"
 62                  },
 63                  "denominator": {
 64                    "value": 1,
 65                    "unit": "Tablet (unit of presentation)",
 66                    "system": "http://snomed.info/sct",
 67                    "code": "732936001"
 68                  }
 69                }
 70              }
 71            ]
 72          }
 73        ],
```
* *indentifier:* Identifiers associated with this Medication Statement that are defined by business processes and/or used to refer to it when a direct URL reference to the resource itself is not appropriate

```
  1 "identifier": [
  2        {
  3          "system": "urn:ietf:rfc:3986",
  4          "value": "urn:uuid:d0f885ca-afa6-4e7e-905d-f7698f9607aa"
  5        }
  6      ],
```
* *status:* A code representing the status of the use of the medication

```
  1 "status": "completed",
```
* *subject:* The person who is taking the medication

```
  1 "subject": {
  2                    "reference": "Patient/69d661eb-e3ed-4e86-b34c-b5e747c13021"
  3                },
```

* *reasonCode:* A reason for why the medication is taken

```
  1 "reasonCode": [{
  2                        "text": "Bluthochdruck/Herz"
  3                    }
```
* *note:* Provides extra information about the medication statement that is not conveyed by the other attributes

```
 1 "note": [
 2         {
 3           "text": "-"
 4         }
 5       ],
```

## Dosage

* *text:* Free text dosage instructions e.g. SIG. (line 3)
* *timing:* when the medication should be taken (line 7 to 16)
* *route:* Indicates the route of administration (line 17 to 25)
* *doseAndRate:* The amount of medication administered (line 26 to 36)
```
  1 "dosage": [
  2          {
  3            "text": "Morgens 1 und abends 1/2 Tablette nehmen"
  4          },
  5          {
  6            "sequence": 1,
  7            "timing": {
  8              "repeat": {
  9                "boundsPeriod": {
 10                  "start": "2012-02-04"
 11                },
 12                "when": [
 13                  "MORN"
 14                ]
 15              }
 16            },
 17            "route": {
 18              "coding": [
 19                {
 20                  "system": "urn:oid:0.4.0.127.0.16.1.1.2.1",
 21                  "code": "20053000",
 22                  "display": "Oral use"
 23                }
 24              ]
 25            },
 26            "doseAndRate": [
 27              {
 28                "doseQuantity": {
 29                  "value": 1,
 30                  "unit": "Tablet (unit of presentation)",
 31                  "system": "http://snomed.info/sct",
 32                  "code": "732936001"
 33                }
 34              }
 35            ]
 36          },
 37          {
 38            "sequence": 2,
 39            "timing": {
 40              "repeat": {
 41                "boundsPeriod": {
 42                  "start": "2012-02-04"
 43                },
 44                "when": [
 45                  "EVE"
 46                ]
 47              }
 48            },
 49            "route": {
 50              "coding": [
 51                {
 52                  "system": "urn:oid:0.4.0.127.0.16.1.1.2.1",
 53                  "code": "20053000",
 54                  "display": "Oral use"
 55                }
 56              ]
 57            },
 58            "doseAndRate": [
 59              {
 60                "doseQuantity": {
 61                  "value": 0.5,
 62                  "unit": "Tablet (unit of presentation)",
 63                  "system": "http://snomed.info/sct",
 64                  "code": "732936001"
 65                }
 66              }
 67            ]
 68          }
 69        ]
 70      }
 71    },
```

The resource "Binary" represents the Medication Card document as PDF

```
  1 "resource": {
  2                "resourceType": "Binary",
  3                "id": "8affdddb-4abc-4e96-9b70-3f4cc3f003cb",
  4                "language": "de-CH",
  5                "contentType": "application/pdf",
  6                "data": "JVBERi0xLjQKMSAwIG9iago8PAovVGl0bGU..."
  7            }
```

# Medication Card document

In a primary system, different medications are documented in a treatment context. Primary systems can use this Exchange Format to generate a Medication Card document with the help of the Content Creator.

## Composite

In the resource "Composition", general information about the document is specified

* *id:* Local id of the resource
* *language:* Specifies the language of the document
* *text:* Presents the narrative text of the resource
* *extension:* Extensions used
* *identifier:* A version-independent identifier for the Composition.
* *status:* The status of the document
* *type:* Specifies the particular kind of composition
* *subject:* Who or what the composition is about.
* *author:* Identifies who is responsible for the information in the composition
* *title:* Human readable label for the composite
* *confidentiality:* Level of confidentiality of the Composition
* *custodian:* Organization who is responsible for the document and access 
* *section:* The root of the sections that make up the composition.

```
"resource": {
        "resourceType": "Composition",
        "id": "2-7-MedicationCard",
        "language": "de-CH",
        "text": {
          "status": "extensions",
          "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\" xml:lang=\"de-CH\" lang=\"de-CH\"><p><b>Generated Narrative</b></p><p><b>EPR Information Recipient</b>: <a href=\"#Patient_MonikaWegmuellerRecipient\">See above (Patient/MonikaWegmuellerRecipient)</a></p><p><b>identifier</b>: id: urn:uuid:6b6ed376-a7da-44cb-92d1-e75ce1ae73b0</p><p><b>status</b>: final</p><p><b>type</b>: <span title=\"Codes: {http://loinc.org 56445-0}, {http://snomed.info/sct 721912009}\">Medication summary</span></p><p><b>date</b>: Feb 4, 2012, 2:05:00 PM</p><p><b>author</b>: </p><ul><li><a href=\"#Practitioner_FamilienHausarzt\">See above (Practitioner/FamilienHausarzt)</a></li><li><a href=\"#Organization_Hausarzt\">See above (Organization/Hausarzt)</a></li></ul><p><b>title</b>: Medikationsplan</p><p><b>confidentiality</b>: N</p><p><b>custodian</b>: <a href=\"#Organization_Custodian\">See above (Organization/Custodian)</a></p></div>"
        },
        "extension": [
          {
            "url": "http://fhir.ch/ig/ch-core/StructureDefinition/ch-ext-epr-informationrecipient",
            "valueReference": {
              "reference": "Patient/MonikaWegmuellerRecipient"
            }
          }
        ],
        "identifier": {
          "system": "urn:ietf:rfc:3986",
          "value": "urn:uuid:6b6ed376-a7da-44cb-92d1-e75ce1ae73b0"
        },
        "status": "final",
        "type": {
          "coding": [
            {
              "system": "http://loinc.org",
              "code": "56445-0",
              "display": "Medication summary"
            },
            {
              "system": "http://snomed.info/sct",
              "code": "721912009",
              "display": "Medication summary document (record artifact)"
            }
          ]
        },
        "subject": {
          "reference": "Patient/MonikaWegmueller"
        },
        "date": "2012-02-04T14:05:00+01:00",
        "author": [
          {
            "extension": [
              {
                "url": "http://fhir.ch/ig/ch-core/StructureDefinition/ch-ext-epr-time",
                "valueDateTime": "2012-02-04T13:55:00+01:00"
              }
            ],
            "reference": "Practitioner/FamilienHausarzt"
          },
          {
            "reference": "Organization/Hausarzt"
          }
        ],
        "title": "Medikationsplan",
        "confidentiality": "N",
        "_confidentiality": {
          "extension": [
            {
              "url": "http://fhir.ch/ig/ch-core/StructureDefinition/ch-ext-epr-confidentialitycode",
              "valueCodeableConcept": {
                "coding": [
                  {
                    "system": "http://snomed.info/sct",
                    "code": "17621005",
                    "display": "Normally accessible"
                  }
                ]
              }
            }
          ]
        },
        "custodian": {
          "reference": "Organization/Custodian"
        },
        "section": [
          {
            "title": "Medikamentenliste",
            "code": {
              "coding": [
                {
                  "system": "http://loinc.org",
                  "code": "10160-0",
                  "display": "History of medication use"
                }
              ]
            },
            "entry": [
              {
                "reference": "MedicationStatement/2-7-MedStatBeloczok"
              },
              {
                "reference": "MedicationStatement/2-7-MedStatNorvasc"
              }
            ]
          },
          {
            "title": "Kommentar",
            "code": {
              "coding": [
                {
                  "system": "http://loinc.org",
                  "code": "48767-8",
                  "display": "Annotation comment"
                }
              ]
            },
            "text": {
              "status": "generated",
              "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\">\n              <span id=\"co1\">\n                  Kommentar zu Medication Treatment\n              </span>\n            </div>"
            }
          },
          {
            "title": "Original Darstellung",
            "code": {
              "coding": [
                {
                  "system": "http://loinc.org",
                  "code": "55108-5",
                  "display": "Clinical presentation"
                }
              ]
            },
            "text": {
              "status": "generated",
              "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\">\n              <a href=\"Binary/2-7-pdf\">Representation of the original view</a>\n            </div>"
            },
            "entry": [
              {
                "reference": "Binary/2-7-pdf"
              }
            ]
          }
        ]
      }
    },
```

## Information about the practitioner

The resource Practionier indicates which Practionier has prescribed a medication

```
"resource": {
                "resourceType": "Practitioner",
                "id": "c23e26e7-cbb9-4155-9117-ae31163c833f",
                "identifier": [{
                        "system": "urn:oid:2.51.1.3",
                        "value": "7601003180268"
                    }
                ],
                "name": [{
                        "family": "Crausaz",
                        "given": ["Christophe"]
                    }
                ]
            }
```

## Information about the patient

In the "Patient" resource, the demographic and administrative data of a patient are specified.

```
"resource": {
                "resourceType": "Patient",
                "id": "69d661eb-e3ed-4e86-b34c-b5e747c13021",
                "identifier": [{
                        "system": "urn:oid:2.99",
                        "value": "1.3.6.1.4.1.21367.2017.2.5.83|MAGMED001"
                    }
                ],
                "name": [{
                        "family": "Muster",
                        "given": ["Petra"]
                    }
                ],
                "telecom": [{
                        "system": "phone",
                        "value": "079 333 22 11"
                    }
                ],
                "gender": "female",
                "birthDate": "1971-09-20",
                "address": [{
                        "line": ["Mustergasse 4"],
                        "city": "Zuerich",
                        "postalCode": "8000"
                    }
                ],
                "communication": [{
                        "language": {
                            "coding": [{
                                    "system": "urn:ietf:bcp:47",
                                    "code": "de-CH"
                                }
                            ]
                        }
                    }
                ]
            }
```
## Information about the organization

The resource stores the information about the organization that create the Medication Card document

```
"resource": {
                "resourceType": "Organization",
                "id": "dc0dead8-eefc-4b94-9a6d-01e521db765c",
                "identifier": [{
                        "system": "urn:oid:2.51.1.3",
                        "value": "7601001362383"
                    }
                ],
                "name": "HCI Solutions AG",
                "address": [{
                        "line": ["Untermattweg 8"],
                        "city": "Bern 1",
                        "postalCode": "3000",
                        "country": "CH"
                    }
                ]
            }
```

## Medication

In the following resource "MedicationStatement" the data of the patient's medication are specified

### Medication information
* *id:* Details of Extension to present additional information
* *status:* Details of Extension to present additional information
* *code:* A code (or set of codes) that specify this medication, or a textual description if no code is available.
* *coding* A reference to a code defined by a terminology system.
* *form* Describes the form of the medication. Powder; tablets; capsule.
* *text:* Human readable text
* *amount:* A relationship of two Quantity values - expressed as a numerator and a denominator.
* *ingredigent:*  Particular ingredient of a medication
* *strength:* A relationship of two Quantity values - expressed as a numerator and a denominator.


```
"resourceType": "MedicationStatement",
        "id": "2-7-MedStatBeloczok",
        "text": {
          "status": "extensions",
          "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\"><p><b>Generated Narrative</b></p><blockquote><p><b>CH EMED Extension Treatment Plan</b></p><h3>Urls</h3><table class=\"grid\"><tr><td>-</td></tr><tr><td>*</td></tr></table><p><b>value</b>: id: urn:uuid:5712fffe-20c6-11e6-b67b-9e71128cae77</p><h3>Urls</h3><table class=\"grid\"><tr><td>-</td></tr><tr><td>*</td></tr></table><p><b>value</b>: id: urn:uuid:5712fffe-20c6-11e6-b67b-9e71128cae77</p></blockquote><p><b>identifier</b>: id: urn:uuid:d0f885ca-afa6-4e7e-905d-f7698f9607aa</p><p><b>status</b>: completed</p><p><b>medication</b>: <a name=\"med\"> </a></p><blockquote><p><b>code</b>: <span title=\"Codes: {urn:oid:2.51.1.1 7680521101306}\">BELOC ZOK Ret Tabl 50 mg</span></p><p><b>form</b>: <span title=\"Codes: {urn:oid:0.4.0.127.0.16.1.1.2.1 10219000}\">Tablet</span></p><p><b>amount</b>: 30 Tablet (unit of presentation)/1 Package</p><h3>Ingredients</h3><table class=\"grid\"><tr><td>-</td><td><b>Item[x]</b></td><td><b>Strength</b></td></tr><tr><td>*</td><td><span title=\"Codes: {http://snomed.info/sct 372826007}\">Metoprolol</span></td><td>50 milligram/1 Tablet (unit of presentation)</td></tr></table></blockquote><p><b>subject</b>: <a href=\"#Patient_MonikaWegmueller\">See above (Patient/MonikaWegmueller)</a></p><p><b>reasonCode</b>: <span title=\"Codes: \">Bluthochdruck</span></p><p><b>note</b>: -</p><h3>Dosages</h3><table class=\"grid\"><tr><td>-</td></tr><tr><td>*</td></tr><tr><td>*</td></tr><tr><td>*</td></tr></table></div>"
        },
        "contained": [
          {
            "resourceType": "Medication",
            "id": "med",
            "code": {
              "coding": [
                {
                  "system": "urn:oid:2.51.1.1",
                  "code": "7680521101306",
                  "display": "BELOC ZOK Ret Tabl 50 mg 30 Stk"
                }
              ],
              "text": "BELOC ZOK Ret Tabl 50 mg"
            },
            "form": {
              "coding": [
                {
                  "system": "urn:oid:0.4.0.127.0.16.1.1.2.1",
                  "code": "10219000",
                  "display": "Tablet"
                }
              ]
            },
            "amount": {
              "numerator": {
                "value": 30,
                "unit": "Tablet (unit of presentation)",
                "system": "http://snomed.info/sct",
                "code": "732936001"
              },
              "denominator": {
                "value": 1,
                "unit": "Package",
                "system": "http://unitsofmeasure.org",
                "code": "{Package}"
              }
            },
            "ingredient": [
              {
                "itemCodeableConcept": {
                  "coding": [
                    {
                      "system": "http://snomed.info/sct",
                      "code": "372826007",
                      "display": "Metoprolol (substance)"
                    }
                  ],
                  "text": "Metoprolol"
                },
                "strength": {
                  "numerator": {
                    "value": 50,
                    "unit": "milligram",
                    "system": "http://unitsofmeasure.org",
                    "code": "mg"
                  },
                  "denominator": {
                    "value": 1,
                    "unit": "Tablet (unit of presentation)",
                    "system": "http://snomed.info/sct",
                    "code": "732936001"
                  }
                }
              }
            ]
          }
        ],
```

## Dosage

* *text:* Free text dosage instructions e.g. SIG.
* *timing:* when the medication should be taken
* *route:* Indicates the route of administration
* *doseAndRate:* The amount of medication administered.
```
"dosage": [
          {
            "text": "Morgens 1 und abends 1/2 Tablette nehmen"
          },
          {
            "sequence": 1,
            "timing": {
              "repeat": {
                "boundsPeriod": {
                  "start": "2012-02-04"
                },
                "when": [
                  "MORN"
                ]
              }
            },
            "route": {
              "coding": [
                {
                  "system": "urn:oid:0.4.0.127.0.16.1.1.2.1",
                  "code": "20053000",
                  "display": "Oral use"
                }
              ]
            },
            "doseAndRate": [
              {
                "doseQuantity": {
                  "value": 1,
                  "unit": "Tablet (unit of presentation)",
                  "system": "http://snomed.info/sct",
                  "code": "732936001"
                }
              }
            ]
          },
          {
            "sequence": 2,
            "timing": {
              "repeat": {
                "boundsPeriod": {
                  "start": "2012-02-04"
                },
                "when": [
                  "EVE"
                ]
              }
            },
            "route": {
              "coding": [
                {
                  "system": "urn:oid:0.4.0.127.0.16.1.1.2.1",
                  "code": "20053000",
                  "display": "Oral use"
                }
              ]
            },
            "doseAndRate": [
              {
                "doseQuantity": {
                  "value": 0.5,
                  "unit": "Tablet (unit of presentation)",
                  "system": "http://snomed.info/sct",
                  "code": "732936001"
                }
              }
            ]
          }
        ]
      }
    },
```

Subject indicates the reference of the patient

```
 "subject": {
                    "reference": "Patient/69d661eb-e3ed-4e86-b34c-b5e747c13021"
                },
```

The "informationSource" indicates which practitioner has prescribed the drug.

```
"informationSource": {
                    "reference": "Practitioner/c23e26e7-cbb9-4155-9117-ae31163c833f"
                },
```

The resonCode indicates the reason for the medication.

```
"reasonCode": [{
                        "text": "Bluthochdruck/Herz"
                    }
```

The dosage of the medication is defined in the following element.

- *timing*: Timing indicates when a drug should be taken
- *route*: Indicates the route of administration
- *doseAndRate*: Indicates the route of administration



```
"dosage": [{
                        "text": "Am Morgen 1 Tabletten. Am Abend 1 Tabletten\r\nMorgens und abends je 1 Tablette nehmen"
                    }, {
                        "timing": {
                            "repeat": {
                                "boundsPeriod": {
                                    "start": "2021-09-20T00:00:00+02:00"
                                },
                                "when": ["MORN", "EVE"]
                            }
                        },
                        "route": {
                            "coding": [{
                                    "system": "urn:oid:0.4.0.127.0.16.1.1.2.1",
                                    "code": "20053000",
                                    "display": "zum Einnehmen"
                                }
                            ]
                        },
                        "doseAndRate": [{
                                "doseQuantity": {
                                    "value": 1,
                                    "unit": "Stk",
                                    "system": "http://unitsofmeasure.org",
                                    "code": "{Piece}"
                                }
                            }
                        ]
                    }
                ]
```
The resource "Binary" represents the Medication Card document as PDF

```
"resource": {
                "resourceType": "Binary",
                "id": "8affdddb-4abc-4e96-9b70-3f4cc3f003cb",
                "language": "de-CH",
                "contentType": "application/pdf",
                "data": "JVBERi0xLjQKMSAwIG9iago8PAovVGl0bGU..."
            }
```

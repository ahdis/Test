# Medication Prescription document

## Composite

In the resource "Composition", general information about the document is specified

```
"resource": {
        "resourceType": "Composition",
        "id": "2-6-MedicationPrescription",
        "language": "de-CH",
        "text": {
          "status": "extensions",
          "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\" xml:lang=\"de-CH\" lang=\"de-CH\"><p><b>Generated Narrative</b></p><p><b>EPR Information Recipient</b>: <a href=\"#Patient_MonikaWegmuellerRecipient\">See above (Patient/MonikaWegmuellerRecipient)</a></p><p><b>identifier</b>: id: urn:uuid:d41d72ba-2100-11e6-b67b-9e71128cae77</p><p><b>status</b>: final</p><p><b>type</b>: <span title=\"Codes: {http://loinc.org 57833-6}, {http://snomed.info/sct 761938008}\">Prescription for medication</span></p><p><b>date</b>: Feb 4, 2012, 2:00:00 PM</p><p><b>author</b>: </p><ul><li><a href=\"#Practitioner_FamilienHausarzt\">See above (Practitioner/FamilienHausarzt)</a></li><li><a href=\"#Organization_Hausarzt\">See above (Organization/Hausarzt)</a></li></ul><p><b>title</b>: Rezept</p><p><b>confidentiality</b>: N</p><p><b>custodian</b>: <a href=\"#Organization_Custodian\">See above (Organization/Custodian)</a></p></div>"
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
          "value": "urn:uuid:d41d72ba-2100-11e6-b67b-9e71128cae77"
        },
        "status": "final",
        "type": {
          "coding": [
            {
              "system": "http://loinc.org",
              "code": "57833-6",
              "display": "Prescription for medication"
            },
            {
              "system": "http://snomed.info/sct",
              "code": "761938008",
              "display": "Medicinal prescription record (record artifact)"
            }
          ]
        },
        "subject": {
          "reference": "Patient/MonikaWegmueller"
        },
        "date": "2012-02-04T14:00:00+01:00",
        "author": [
          {
            "extension": [
              {
                "url": "http://fhir.ch/ig/ch-core/StructureDefinition/ch-ext-epr-time",
                "valueDateTime": "2012-02-04T14:00:00+01:00"
              }
            ],
            "reference": "Practitioner/FamilienHausarzt"
          },
          {
            "reference": "Organization/Hausarzt"
          }
        ],
        "title": "Rezept",
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
            "title": "Arzneimittelverordnung",
            "code": {
              "coding": [
                {
                  "system": "http://loinc.org",
                  "code": "57828-6",
                  "display": "PRESCRIPTIONS"
                }
              ]
            },
            "entry": [
              {
                "reference": "MedicationRequest/2-6-MedReqNorvasc"
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
              "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\">\n                     <span id=\"co1\">\n\t\t\t\t\t\tKommentar zu Medication Prescription\n                     </span>\n                  </div>"
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
              "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\">\n                     <a href=\"Binary/2-6-pdf\">Representation of the original view</a>\n                  </div>"
            },
            "entry": [
              {
                "reference": "Binary/2-6-pdf"
              }
            ]
          }
        ]
      }
```

## Information about patient

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

## Information about practitioner

```
"resource": {
        "resourceType": "Practitioner",
        "id": "FamilienHausarzt",
        "text": {
          "status": "generated",
          "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\"><p><b>Generated Narrative</b></p><p><b>identifier</b>: id: 7601000234438</p><p><b>name</b>: Familien Hausarzt </p></div>"
        },
        "identifier": [
          {
            "system": "urn:oid:2.51.1.3",
            "value": "7601000234438"
          }
        ],
        "name": [
          {
            "family": "Hausarzt",
            "given": [
              "Familien"
            ]
          }
        ]
      }
    },
```

## Information about organization

```
 "resource": {
        "resourceType": "Organization",
        "id": "Hausarzt",
        "text": {
          "status": "generated",
          "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\"><p><b>Generated Narrative</b></p><p><b>identifier</b>: id: 7601000234438</p><p><b>name</b>: Hausarzt</p><p><b>address</b>: Krankenstrasse 2 Zürich 8005 CH </p></div>"
        },
        "identifier": [
          {
            "system": "urn:oid:2.51.1.3",
            "value": "7601000234438"
          }
        ],
        "name": "Hausarzt",
        "address": [
          {
            "line": [
              "Krankenstrasse 2"
            ],
            "city": "Zürich",
            "postalCode": "8005",
            "country": "CH"
          }
        ]
      }
    },
```

## Medication

In the following resource "MedicationStatement" the data of the patient's medication are specified

### Medication information

Medication Coded from the "urn:oid:2.51.1.1" system

```
"code": {
                            "coding": [{
                                    "system": "urn:oid:2.51.1.1",
                                    "code": "7680500440334",
                                    "display": "Norvasc Tabl 10 mg 30 Stk"
                                }
                            ],
                            "text": "Norvasc Tabl 10 mg 30 Stk"
                        },
```

Indication of dosage form

```
 "form": {
                            "coding": [{
                                    "system": "urn:oid:0.4.0.127.0.16.1.1.2.1",
                                    "code": "10219000",
                                    "display": "Tablette"
                                }
                            ],
                            "text": "Tablette"
                        },
```
Number of tablets per package with indication of the unit

```
"amount": {
                            "numerator": {
                                "value": 30,
                                "unit": "Stk",
                                "system": "http://unitsofmeasure.org",
                                "code": "{Piece}"
                            },
                            "denominator": {
                                "value": 1,
                                "unit": "Packung",
                                "system": "http://unitsofmeasure.org",
                                "code": "{Package}"
                            }
                        },
```
The following element shows the ingredients of the medication.
The ingredient is defined with value and unit for the active ingredient quantity.

```
"ingredient": [{
                                "itemCodeableConcept": {
                                    "coding": [{
                                            "system": "http://snomed.info/sct",
                                            "code": "386864001",
                                            "display": "Amlodipine"
                                        }
                                    ],
                                    "text": "Amlodipin"
                                },
                                "strength": {
                                    "numerator": {
                                        "value": 10,
                                        "unit": "mg",
                                        "system": "http://unitsofmeasure.org",
                                        "code": "mg"
                                    },
                                    "denominator": {
                                        "value": 1,
                                        "unit": "Stk",
                                        "system": "http://unitsofmeasure.org",
                                        "code": "{Piece}"
                                    }
                                }
                            }
                        ]
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
        "id": "2-6-pdf",
        "language": "de-CH",
        "contentType": "application/pdf",
        "data": "JVBERi0xLjQNJeLjz9M..."
      }
```

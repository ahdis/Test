# Medication Dispense document

## Composite
In the resource "Composition", general information about the document is specified,

```
"resourceType": "Composition",
        "id": "1-2-MedicationDispense",
        "language": "de-CH",
        "text": {
          "status": "extensions",
          "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\" xml:lang=\"de-CH\" lang=\"de-CH\"><p><b>Generated Narrative</b></p><p><b>EPR Information Recipient</b>: <a href=\"#Patient_MonikaWegmuellerRecipient\">See above (Patient/MonikaWegmuellerRecipient)</a></p><p><b>identifier</b>: id: urn:uuid:488bd23a-20c6-11e6-b67b-9e71128cae77</p><p><b>status</b>: final</p><p><b>type</b>: <span title=\"Codes: {http://loinc.org 60593-1}, {http://snomed.info/sct 419891008}\">Medication dispensed.extended</span></p><p><b>date</b>: Nov 29, 2011, 11:01:00 AM</p><p><b>author</b>: </p><ul><li><a href=\"#Practitioner_FamilienHausarzt\">See above (Practitioner/FamilienHausarzt)</a></li><li><a href=\"#Organization_Hausarzt\">See above (Organization/Hausarzt)</a></li></ul><p><b>title</b>: Abgabe</p><p><b>confidentiality</b>: N</p><p><b>custodian</b>: <a href=\"#Organization_Custodian\">See above (Organization/Custodian)</a></p></div>"
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
          "value": "urn:uuid:488bd23a-20c6-11e6-b67b-9e71128cae77"
        },
        "status": "final",
        "type": {
          "coding": [
            {
              "system": "http://loinc.org",
              "code": "60593-1",
              "display": "Medication dispensed.extended"
            },
            {
              "system": "http://snomed.info/sct",
              "code": "419891008",
              "display": "Record artifact (record artifact)"
            }
          ]
        },
        "subject": {
          "reference": "Patient/MonikaWegmueller"
        },
        "date": "2011-11-29T11:01:00+01:00",
        "author": [
          {
            "extension": [
              {
                "url": "http://fhir.ch/ig/ch-core/StructureDefinition/ch-ext-epr-time",
                "valueDateTime": "2011-11-29T11:00:00+01:00"
              }
            ],
            "reference": "Practitioner/FamilienHausarzt"
          },
          {
            "reference": "Organization/Hausarzt"
          }
        ],
        "title": "Abgabe",
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
            "title": "Abgabe eines Medikaments",
            "code": {
              "coding": [
                {
                  "system": "http://loinc.org",
                  "code": "60590-7",
                  "display": "Medication dispensed.brief"
                }
              ]
            },
            "text": {
              "status": "generated",
              "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\">\n                            <table>\n                                <thead>\n                                    <tr>\n                                        <th>Präpartename</th>\n                                        <th>Wirkstoffname</th>\n                                        <th>Galenische Form</th>\n                                        <th>Dosis pro Einheit</th>\n                                        <th>Anzahl Packungen</th>\n                                        <th>Packungsgrösse</th>\n                                        <th>Dosierung</th>\n                                        <th>Dos.Morgen</th>\n                                        <th>Dos.Mittag</th>\n                                        <th>Dos.Abend</th>\n                                        <th>Dos.Nacht</th>\n                                        <th>Verabreichungsweg</th>\n                                        <th>Kommentar</th>\n                                        <th>Behandlungsrund</th>\n                                        <th>Datum/Zeit der Abgabe/ Anwendung</th>\n                                        <th>Identifikation des Empfängers</th>\n                                    </tr>\n                                </thead>\n                                <tbody>\n                                    <tr id=\"dis.1\">\n                                        <td id=\"dis.1.brandedmedication\">Triatec</td>\n                                        <td id=\"dis.1.ingredient\">Ramipril</td>\n                                        <td id=\"dis.1.dosequantity\">2.5 mg</td>\n                                        <td id=\"dis.1.packageform\">Tbl</td>\n                                        <td id=\"dis.1.nopackages\">1</td>\n                                        <td id=\"dis.1.packagesize\">20</td>\n                                        <td id=\"dis.1.dosageintakemode\">Morgens 1/2 Tablette nehmen</td>\n                                        <td id=\"dis.1.dosagemorning\">0.5</td>\n                                        <td id=\"dis.1.dosagelunch\">0</td>\n                                        <td id=\"dis.1.dosageevening\">0</td>\n                                        <td id=\"dis.1.dosagenight\">0</td>\n                                        <td id=\"dis.1.routecode\">oral</td>\n                                        <td id=\"dis.1.note\"/>\n                                        <td id=\"dis.1.datefromto\"/>\n                                        <td id=\"dis.1.reason\">Bluthochdruck</td>\n                                        <td id=\"dis.1.dipsensedate\"/>\n                                        <td id=\"dis.1.dipsenseto\"/>\n                                    </tr>\n                                </tbody>\n                            </table>\n                        </div>"
            },
            "entry": [
              {
                "reference": "MedicationDispense/1-2-MedDispTriatec"
              }
            ]
          }
        ]
      }
    },
```


```
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

## Information about the organization

The resource stores the information about the organization that create the Medication Card document.

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

## Information about the patient

In the "Patient" resource, the demographic and administrative data of a patient are specified.

```
"resource": {
        "resourceType": "Patient",
        "id": "MonikaWegmuellerRecipient",
        "text": {
          "status": "generated",
          "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\"><p><b>Generated Narrative</b></p><p><b>name</b>: Monika Wegmüller </p><p><b>address</b>: Wiesenstr. 12 Zürich 8003 CH </p></div>"
        },
        "name": [
          {
            "family": "Wegmüller",
            "given": [
              "Monika"
            ]
          }
        ],
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

## Medication Dispense

In the resource "MedicationDispens" the information of the medication to be dispensed is defined. It contains the resoruce "Medication".

## Medication

```
"resourceType": "Medication",
            "id": "med",
            "code": {
              "extension": [
                {
                  "url": "http://hl7.org/fhir/StructureDefinition/narrativeLink",
                  "valueUrl": "#dis.1.brandedmedication"
                }
              ],
              "coding": [
                {
                  "system": "urn:oid:2.51.1.1",
                  "code": "7680538751228",
                  "display": "TRIATEC Tabl 2.5 mg 20 Stk"
                }
              ],
              "text": "TRIATEC Tabl 2.5 mg"
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
                "value": 20,
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
                      "code": "386872004",
                      "display": "Ramipril (substance)"
                    }
                  ],
                  "text": "Ramipril"
                },
                "strength": {
                  "numerator": {
                    "value": 2.5,
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
        "extension": [
          {
            "url": "http://hl7.org/fhir/StructureDefinition/narrativeLink",
            "valueUrl": "#dis.1"
          },
          {
            "url": "http://fhir.ch/ig/ch-emed/StructureDefinition/ch-emed-ext-treatmentplan",
            "extension": [
              {
                "url": "id",
                "valueIdentifier": {
                  "system": "urn:ietf:rfc:3986",
                  "value": "urn:uuid:c9f758a1-296c-4710-84d4-e181db8c7478"
                }
              },
              {
                "url": "externalDocumentId",
                "valueIdentifier": {
                  "system": "urn:ietf:rfc:3986",
                  "value": "urn:uuid:c9f758a1-296c-4710-84d4-e181db8c7478"
                }
              }
            ]
          }
        ],
        "identifier": [
          {
            "system": "urn:ietf:rfc:3986",
            "value": "urn:uuid:488bd23a-20c6-11e6-b67b-9e71128cae77"
          }
        ],
        "status": "completed",
        "medicationReference": {
          "reference": "#med"
        },
        "subject": {
          "reference": "Patient/MonikaWegmueller"
        },
        "quantity": {
          "value": 1
        },
        "dosageInstruction": [
          {
            "timing": {
              "repeat": {
                "boundsPeriod": {
                  "start": "2011-11-29"
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
                  "value": 0.5,
                  "unit": "Tablet (unit of presentation)",
                  "system": "http://snomed.info/sct",
                  "code": "732936001"
                }
              }
            ]
          },
          {
            "extension": [
              {
                "url": "http://hl7.org/fhir/StructureDefinition/narrativeLink",
                "valueUrl": "#dis.1.dosageintakemode"
              }
            ],
            "text": "Morgens 1/2 Tablette nehmen"
          }
        ]
      }
```

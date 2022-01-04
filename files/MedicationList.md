# Medication List document

## Composite

In the resource "Composition", general information about the document is specified.

```
 "resource": {
        "resourceType": "Composition",
        "language": "de-CH",
        "text": {
          "status": "extensions",
          "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\" xml:lang=\"de-CH\" lang=\"de-CH\"><p><b>Generated Narrative</b></p><p><b>EPR Information Recipient</b>: <a href=\"#urnuuide89c0e17-a3af-4179-a089-1a2189f5241c\">See above (Patient/null)</a></p><p><b>identifier</b>: id: urn:uuid:17931678-20b4-11e6-b67b-9e71128cae77</p><p><b>status</b>: final</p><p><b>type</b>: <span title=\"Codes: {http://loinc.org 56445-0}, {http://snomed.info/sct 721912009}\">Medication summary</span></p><p><b>date</b>: Feb 4, 2012, 1:55:00 PM</p><p><b>author</b>: </p><ul><li><a href=\"#urnuuid9689296c-7861-44d4-8824-714f2917c8c9\">See above (Practitioner/null)</a></li><li><a href=\"#urnuuid76c1ea57-0834-4f52-b87b-8b534e9918f2\">See above (Organization/null)</a></li></ul><p><b>title</b>: Medikationsliste</p><p><b>confidentiality</b>: N</p><p><b>custodian</b>: <a href=\"#urnuuidc7ab130a-7962-47f8-bd62-4f40e0099f4d\">See above (Organization/null)</a></p></div>"
        },
        "extension": [
          {
            "url": "http://fhir.ch/ig/ch-core/StructureDefinition/ch-ext-epr-informationrecipient",
            "valueReference": {
              "reference": "urn:uuid:e89c0e17-a3af-4179-a089-1a2189f5241c"
            }
          }
        ],
        "identifier": {
          "system": "urn:ietf:rfc:3986",
          "value": "urn:uuid:17931678-20b4-11e6-b67b-9e71128cae77"
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
          "reference": "urn:uuid:1848022e-bf1c-4421-bb4c-b803522c3411"
        },
        "date": "2012-02-04T13:55:00+01:00",
        "author": [
          {
            "extension": [
              {
                "url": "http://fhir.ch/ig/ch-core/StructureDefinition/ch-ext-epr-time",
                "valueDateTime": "2012-02-04T13:55:00+01:00"
              }
            ],
            "reference": "urn:uuid:9689296c-7861-44d4-8824-714f2917c8c9"
          },
          {
            "reference": "urn:uuid:76c1ea57-0834-4f52-b87b-8b534e9918f2"
          }
        ],
        "title": "Medikationsliste",
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
          "reference": "urn:uuid:c7ab130a-7962-47f8-bd62-4f40e0099f4d"
        },
        "section": [
          {
            "extension": [
              {
                "url": "http://fhir.ch/ig/ch-core/StructureDefinition/ch-ext-epr-sectionid",
                "valueIdentifier": {
                  "system": "urn:ietf:rfc:3986",
                  "value": "urn:uuid:f5ee14ee-52dc-48b0-8d96-e2713c99e607"
                }
              }
            ],
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
            "text": {
              "status": "generated",
              "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\">\n                            <table>\n                                <thead>\n                                    <tr>\n                                        <th>Typ des Dokuments</th>\n                                        <th>Präpartename</th>\n                                        <th>Wirkstoffname</th>\n                                        <th>Galenische Form</th>\n                                        <th>Dosis pro Einheit</th>\n                                        <th>Dosierung</th>\n                                        <th>Dos.Morgen</th>\n                                        <th>Dos.Mittag</th>\n                                        <th>Dos.Abend</th>\n                                        <th>Dos.Nacht</th>\n                                        <th>Verabreichungsweg</th>\n                                        <th>Kommentar</th>\n                                        <th>Anwendungsdauer</th>\n                                        <th>Behandlungsgrund</th>\n                                    </tr>\n                                </thead>\n                                <tbody>\n                                    <tr id=\"mtp.1\">\n                                        <td id=\"mtp.1.documenttype\">Medication Treatment Plan document</td>\n                                        <td id=\"mtp.1.brandedmedication\">Triatec</td>\n                                        <td id=\"mtp.1.ingredient\">Ramipril</td>\n                                        <td id=\"mtp.1.packageform\">Tbl</td>\n                                        <td id=\"mtp.1.dosequantity\">2.5 mg</td>\n                                        <td id=\"mtp.1.dosageintakemode\">Morgens 1/2 Tablette nehmen</td>\n                                        <td id=\"mtp.1.dosagemorning\">0.5</td>\n                                        <td id=\"mtp.1.dosagelunch\">0</td>\n                                        <td id=\"mtp.1.dosageevening\">0</td>\n                                        <td id=\"mtp.1.dosagenight\">0</td>\n                                        <td id=\"mtp.1.routecode\">oral</td>\n                                        <td id=\"mtp.1.note\"/>\n                                        <td id=\"mtp.1.datefromto\"/>\n                                        <td id=\"mtp.1.reason\">Bluthochdruck</td>\n                                    </tr>\n                                </tbody>\n                            </table>\n                            <table>\n                                <thead>\n                                    <tr>\n                                        <th>Typ des Dokuments</th>\n                                        <th>Präpartename</th>\n                                        <th>Wirkstoffname</th>\n                                        <th>Galenische Form</th>\n                                        <th>Dosis pro Einheit</th>\n                                        <th>Anzahl Packungen</th>\n                                        <th>Packungsgrösse</th>\n                                        <th>Dosierung</th>\n                                        <th>Dos.Morgen</th>\n                                        <th>Dos.Mittag</th>\n                                        <th>Dos.Abend</th>\n                                        <th>Dos.Nacht</th>\n                                        <th>Verabreichungsweg</th>\n                                        <th>Kommentar</th>\n                                        <th>Behandlungsrund</th>\n                                        <th>Datum/Zeit der Abgabe/ Anwendung</th>\n                                        <th>Identifikation des Empfängers</th>\n                                    </tr>\n                                </thead>\n                                <tbody>\n                                    <tr id=\"dis.1\">\n                                        <td id=\"dis.1.documenttype\">Medication Dispense document</td>\n                                        <td id=\"dis.1.brandedmedication\">Triatec</td>\n                                        <td id=\"dis.1.ingredient\">Ramipril</td>\n                                        <td id=\"dis.1.dosequantity\">2.5 mg</td>\n                                        <td id=\"dis.1.packageform\">Tbl</td>\n                                        <td id=\"dis.1.nopackages\">1</td>\n                                        <td id=\"dis.1.packagesize\">20</td>\n                                        <td id=\"dis.1.dosageintakemode\">Morgens 1/2 Tablette nehmen</td>\n                                        <td id=\"dis.1.dosagemorning\">0.5</td>\n                                        <td id=\"dis.1.dosagelunch\">0</td>\n                                        <td id=\"dis.1.dosageevening\">0</td>\n                                        <td id=\"dis.1.dosagenight\">0</td>\n                                        <td id=\"dis.1.routecode\">oral</td>\n                                        <td id=\"dis.1.note\"/>\n                                        <td id=\"dis.1.datefromto\"/>\n                                        <td id=\"dis.1.reason\">Bluthochdruck</td>\n                                        <td id=\"dis.1.dipsensedate\"/>\n                                        <td id=\"dis.1.dipsenseto\"/>\n                                    </tr>\n                                </tbody>\n                            </table>\n                        </div>"
            },
            "entry": [
              {
                "reference": "urn:uuid:733f5a67-5347-43bb-a3e1-068b10a0d808"
              },
              {
                "reference": "urn:uuid:97ebd6b4-f0d9-4ee6-a81b-0853c259d5b6"
              }
            ]
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

## MedicationStatement

## Medication

```
{
            "resourceType": "Medication",
            "id": "med",
            "code": {
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
"dosage": [
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
                "valueUrl": "#mtp.1.dosageintakemode"
              }
            ],
            "text": "Morgens 1/2 Tablette nehmen"
          }
        ]
```

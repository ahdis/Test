# Medication Card document

In a primary system, different medications are documented in a treatment context. Primary systems can use this Exchange Format to generate a Medication Card document with the help of the Content Creator.

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
                "id": "8affdddb-4abc-4e96-9b70-3f4cc3f003cb",
                "language": "de-CH",
                "contentType": "application/pdf",
                "data": "JVBERi0xLjQKMSAwIG9iago8PAovVGl0bGU..."
            }
```

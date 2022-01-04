# Create Medication Card document

In a primary system, different medications are documented in a treatment context. Primary systems can use this transaction to generate a Medication Card document with the help of the Content Creator.

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


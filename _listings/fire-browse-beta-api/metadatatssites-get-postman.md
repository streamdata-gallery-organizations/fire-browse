{
  "info": {
    "name": "Fire Browse Beta API Obtain identities of tissue source sites in TCGA.",
    "_postman_id": "15b717fb-05dc-425e-a22e-b9bcf20dd385",
    "description": "By default this function returns a table of all sites which contributed source tissue to TCGA, aka TSS's. A subset of this table may be obtained by explicitly specifying one or more sites.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Archives",
      "item": [
        {
          "id": "b45302d7-baa2-444c-8a61-2d29d6c6885b",
          "name": "getArchivesStandarddata",
          "request": {
            "url": "http://firebrowse.org/api/v1/Archives/StandardData?center=%7B%7D&cohort=%7B%7D&data_type=%7B%7D&date=%7B%7D&format=%7B%7D&level=%7B%7D&page=%7B%7D&page_size=%7B%7D&platform=%7B%7D&protocol=%7B%7D&sort_by=%7B%7D&tool=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service returns the archive URLs for our Firehose standard data runs, providing a RESTful interface similar in spirit to the command line firehose_get tool. The archives can be filtered based on date, cohort, data type, platform, center, data level, and protocol."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "198bb236-1c56-41b9-bdac-fc530bebcc74"
            }
          ]
        }
      ]
    },
    {
      "name": "Metadata",
      "item": [
        {
          "id": "45ab9e4d-d7e9-49d3-87a5-8846334c992d",
          "name": "getMetadataCenters",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/Centers?center=%7B%7D&format=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "By default this function returns a table of all consortium members in TCGA, aka centers; it provides both the HTTP domain and full organizational name of each center.  A subset of this table may be obtained by explicitly specifying one or more domain names."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c35cc82a-3829-4d36-9cd0-4200248f3c7b"
            }
          ]
        },
        {
          "id": "677e1c5d-4fe8-4a8a-9999-3a1cd38908ef",
          "name": "getMetadataClinicalnames",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/ClinicalNames?format=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve names of all patient-level clinical data elements (CDES) available in TCGA, unioned across all disease cohorts. A CDE will be listed here only when it has a value other than NA for at least 1 patient case in any disease cohort. For more information on how these CDEs are processed see our pipeline documentation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bd704850-61de-4dc6-b163-de512088bb9f"
            }
          ]
        },
        {
          "id": "dffe44e2-c101-48ab-9f47-ad6efc6bbaed",
          "name": "getMetadataClinicalnamesFh",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/ClinicalNames_FH?format=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service returns the names of patient-level clinical data elements (CDEs) that have been normalized by Firehose for use in analyses, unioned across all disease cohorts. For more information on how these CDEs are processed, see our pipeline documentation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d272c872-3ec2-4ee0-af9c-71697d799d6a"
            }
          ]
        },
        {
          "id": "686cbd11-c9c4-4337-8b6f-490e19a85764",
          "name": "getMetadataCohorts",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/Cohorts?cohort=%7B%7D&format=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "By default this function returns a table containing all TCGA cohort abbreviations and their corresponding disease names.  A subset of that table may be obtained by explicitly specifying one or more cohort abbreviations."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e3574d13-c3d6-456e-ad21-d90999b7c8ed"
            }
          ]
        },
        {
          "id": "f47a02f8-4c66-4aff-bba9-9e8012ed61c7",
          "name": "getMetadataCounts",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/Counts?cohort=%7B%7D&data_type=%7B%7D&date=%7B%7D&format=%7B%7D&sample_type=%7B%7D&sort_by=%7B%7D&totals=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the aliquot counts for each disease cohort, per sample\ntype and data type.  The sample type designation of \"Tumor\"\nmay be used to aggregate the count of all tumor aliquots into\na single number per disease and data type. See the SampleTypes\nfunction for a complete description of sample types."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "56da548e-d231-45a4-98ee-9f62ee0779cf"
            }
          ]
        },
        {
          "id": "c003848e-f442-4082-a744-f1f46c4a6af9",
          "name": "getMetadataDates",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/Dates?format=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve datestamps of all gdac firehose standard data and analyses runs that have been ingested into firebrowse.."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ddaaec37-5694-45e5-98a8-b6e69121b0a7"
            }
          ]
        },
        {
          "id": "a197d57b-9882-4bcc-ac56-214abb1ccdc9",
          "name": "getMetadataHeartbeat",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/HeartBeat?format=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a message to indicate that API (server) is up and running, or times out if not."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b6e8f5d3-dda9-45e7-a4a8-1320a83d54eb"
            }
          ]
        },
        {
          "id": "83018a0a-6cd0-4f7a-8f70-5ce0826a73ea",
          "name": "getMetadataMafcolnames",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/MAFColNames?format=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve the names of all columns in the mutation annotation files (MAFs) hosted by FireBrowse.  For more information on the mutation data, and how it is processed by Firehose, please consult the pipeline documentation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8e5d23e8-ffaf-4d76-a0e0-266fef09f454"
            }
          ]
        },
        {
          "id": "bbbd3398-c2b5-4c81-88d8-58e031d2ef2a",
          "name": "getMetadataPatients",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/Patients?cohort=%7B%7D&format=%7B%7D&page=%7B%7D&page_size=%7B%7D&sort_by=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service returns a list of all TCGA patient barcodes in FireBrowse, optionally filtered by disease cohort.  The barcodes are obtained directy from the clinical data."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "632dd29f-10aa-4aa8-9650-64d943c6accb"
            }
          ]
        },
        {
          "id": "8ed64924-58a4-47be-9309-613f423fb2da",
          "name": "getMetadataPlatforms",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/Platforms?format=%7B%7D&platform=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "By default this function returns a table of all of the technology platforms used to sequence or characterize samples in TCGA--both their short platform codes and full names.  A subset of this table may be obtained by explicitly specifying one or more platform codes."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b38468e1-7b89-4e5d-b54e-ca2cfb73383f"
            }
          ]
        },
        {
          "id": "9871592c-5424-47c8-b234-ed7da30a9609",
          "name": "getMetadataSampletypeBarcodeTcgaBarcode",
          "request": {
            "url": {
              "protocol": "http",
              "host": "firebrowse.org",
              "path": [
                "api",
                "v1",
                "Metadata/SampleType/Barcode/:TCGA_Barcode"
              ],
              "query": [
                {
                  "key": "format",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "TCGA_Barcode",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Given a tcga barcode, return its short letter sample type code.."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cf3c006d-1ec3-44fa-a3a8-9fa071560586"
            }
          ]
        },
        {
          "id": "b88bb2de-c612-4518-bb6d-3a903813dc5b",
          "name": "getMetadataSampletypeCodeCode",
          "request": {
            "url": {
              "protocol": "http",
              "host": "firebrowse.org",
              "path": [
                "api",
                "v1",
                "Metadata/SampleType/Code/:code"
              ],
              "query": [
                {
                  "key": "format",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "code",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Convert a TCGA numeric sample type code (e.g. 01, 02) to its corresponding symbolic (short letter) code (e.g. TP, TR)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c5c284c2-74f3-49a8-8e96-251c4db1bd1b"
            }
          ]
        },
        {
          "id": "b14c3fca-90aa-42fc-88f3-846d9d14d662",
          "name": "getMetadataSampletypeShortlettercodeShortLetterCode",
          "request": {
            "url": {
              "protocol": "http",
              "host": "firebrowse.org",
              "path": [
                "api",
                "v1",
                "Metadata/SampleType/ShortLetterCode/:short_letter_code"
              ],
              "query": [
                {
                  "key": "format",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "short_letter_code",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Convert a TCGA sample type code in symbolic form (or 'short letter code' like TP, TR) to its corresponding numeric form (e.g. 01, 02)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "672f2dc2-e92b-4ce7-86c4-9a725fa9d38d"
            }
          ]
        },
        {
          "id": "3fbe3296-11e5-4a43-8dc5-fb2146e7cb13",
          "name": "getMetadataSampletypes",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/SampleTypes?format=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Return all tcga sample type codes, both numeric and symbolic.."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f5327c6f-486d-46f5-ba82-d9118a7dd2d7"
            }
          ]
        },
        {
          "id": "494398fb-65fa-4066-9d50-98b811ee7eee",
          "name": "getMetadataTssites",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/TSSites?format=%7B%7D&tss_code=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "By default this function returns a table of all sites which contributed source tissue to TCGA, aka TSS's. A subset of this table may be obtained by explicitly specifying one or more sites."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ed4dda6a-a9c1-4a16-bc9e-7f26a0f71d2c"
            }
          ]
        }
      ]
    }
  ]
}
{
  "info": {
    "name": "Fire Browse Beta API Return all TCGA sample type codes, both numeric and symbolic.",
    "_postman_id": "eced0b9e-d1c0-42c4-acf9-c2017ff3220e",
    "description": "Return all tcga sample type codes, both numeric and symbolic..",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Archives",
      "item": [
        {
          "id": "c4d8a872-4599-414e-95e2-030e5cf500bb",
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
              "id": "829b02bd-d196-4cf2-891d-5db2d4f93b29"
            }
          ]
        }
      ]
    },
    {
      "name": "Metadata",
      "item": [
        {
          "id": "2f38a238-c550-402d-a2e1-bb6591c49c5c",
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
              "id": "2cb35be5-7f9e-415c-9c95-4be9e310f51c"
            }
          ]
        },
        {
          "id": "a288590a-e00b-48bb-bef4-431b674d0f05",
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
              "id": "c3bb4859-dc95-4133-a108-0d25e3111e4b"
            }
          ]
        },
        {
          "id": "f456f6dd-aada-48d5-b706-787f22bbd1d8",
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
              "id": "c04a435d-bbcf-4772-acdb-def75e84fb3c"
            }
          ]
        },
        {
          "id": "e1b197b7-79d7-4b39-a9a7-094eb5a41e91",
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
              "id": "7f0f1ed8-ebb6-44b3-927d-fe3f00f87451"
            }
          ]
        },
        {
          "id": "612468ab-f8f5-47cd-8512-85d31d179af6",
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
              "id": "201b8df8-0d67-425d-9054-4db4522b4f25"
            }
          ]
        },
        {
          "id": "da058368-1489-4639-9c6d-aa3ab3efb490",
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
              "id": "0618c348-f286-47b2-981a-5f8d5414c8ff"
            }
          ]
        },
        {
          "id": "5040f4ea-0351-48d8-99c0-3584b087956a",
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
              "id": "8adbc29e-aa5a-4bd9-ba02-507c96fd47ef"
            }
          ]
        },
        {
          "id": "b4a34b2e-b47e-4eae-b35d-83396d5c642a",
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
              "id": "e7b09153-69d5-470d-aa56-e20c09611cb8"
            }
          ]
        },
        {
          "id": "9bb926e9-b5d6-48d7-9d43-9690dfc26daf",
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
              "id": "8eddc00c-80d5-4115-bce1-ce373c365de6"
            }
          ]
        },
        {
          "id": "32ffad71-707a-4109-be73-d329f53925a0",
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
              "id": "56a21f43-57ca-4d6b-80e6-c4342045d45d"
            }
          ]
        },
        {
          "id": "5fea2266-ecc2-4203-8ec8-c228412e3d94",
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
              "id": "213f618c-b54b-465c-9c05-ade2ed609060"
            }
          ]
        },
        {
          "id": "40433363-271a-45b8-a5ef-97cd0cfbcdbb",
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
              "id": "934328fe-0083-49c0-8745-1da96035414e"
            }
          ]
        },
        {
          "id": "638fce4e-7c3a-4b11-8140-3f4d0a6b3351",
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
              "id": "0ddf3858-bc35-45c5-962d-05a05f8aea4e"
            }
          ]
        },
        {
          "id": "c0d1ae9c-c280-4944-a316-a0f76b01110a",
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
              "id": "befd074e-e16d-4c8d-b898-e989884dbc46"
            }
          ]
        }
      ]
    }
  ]
}
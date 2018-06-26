{
  "info": {
    "name": "Fire Browse Beta API Translate TCGA platform codes to full platform names.",
    "_postman_id": "1875c692-0d86-499e-b387-d51276f55c9c",
    "description": "By default this function returns a table of all of the technology platforms used to sequence or characterize samples in TCGA--both their short platform codes and full names.  A subset of this table may be obtained by explicitly specifying one or more platform codes.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Archives",
      "item": [
        {
          "id": "60857981-e9bf-4b53-8aac-5a16765f37db",
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
              "id": "a2e37051-ac0c-4e3d-9575-9bb2aad0e55c"
            }
          ]
        }
      ]
    },
    {
      "name": "Metadata",
      "item": [
        {
          "id": "276ca707-8bdf-4398-8e8b-ca2bf960957e",
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
              "id": "c3fa949f-793c-4fbf-9266-cecb0044948b"
            }
          ]
        },
        {
          "id": "fd015692-795d-4b9a-9eca-b311bd4976ee",
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
              "id": "b3c3bd17-dce7-4359-b038-0f034496ccf6"
            }
          ]
        },
        {
          "id": "c9234c64-e1e7-4643-a5b6-8c49bb43ccd0",
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
              "id": "781b0fa7-7e92-41e8-ba13-498cb8044864"
            }
          ]
        },
        {
          "id": "9e9d6823-a832-49f9-8b80-689c51fd1186",
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
              "id": "4e96082c-25bf-445f-851b-70246e836040"
            }
          ]
        },
        {
          "id": "960d36bf-ba81-4405-904b-440c8165de9e",
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
              "id": "e728ad86-58cc-485c-9f43-b3376b4d9cfe"
            }
          ]
        },
        {
          "id": "07643db1-46ae-48b9-8821-70a704da86ec",
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
              "id": "039dcf8a-bfe5-4a21-972e-c0eef9772c7c"
            }
          ]
        },
        {
          "id": "1c924969-7895-4fc4-b7cd-e5a547456f88",
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
              "id": "56c8c9dc-e110-4c13-ad22-56b458e484fa"
            }
          ]
        },
        {
          "id": "bebd11d2-3a88-4788-bd9f-28900595504f",
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
              "id": "3d653599-1ad1-4329-8675-097edfddae65"
            }
          ]
        },
        {
          "id": "734dcfee-626d-4358-a0ff-1e3db5c50725",
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
              "id": "a091eb9a-63dc-4a4f-af60-2384dde5b139"
            }
          ]
        },
        {
          "id": "d94c0385-495f-478e-8889-71e53a9b2571",
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
              "id": "42f2e0dd-2754-4d52-ac3e-101511326fe1"
            }
          ]
        }
      ]
    }
  ]
}
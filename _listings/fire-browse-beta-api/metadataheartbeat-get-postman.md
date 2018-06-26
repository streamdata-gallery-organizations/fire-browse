{
  "info": {
    "name": "Fire Browse Beta API Simple way to discern whether API server is up and running",
    "_postman_id": "24047d2c-93e9-413b-9a96-1e6140e9e44f",
    "description": "Returns a message to indicate that API (server) is up and running, or times out if not.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Archives",
      "item": [
        {
          "id": "02d1c11a-aba8-4006-ad92-3cd0b6ed1029",
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
              "id": "eb167e07-51fd-475b-9868-e52a2fa7487d"
            }
          ]
        }
      ]
    },
    {
      "name": "Metadata",
      "item": [
        {
          "id": "50b7887b-ad2b-43dc-8471-a85775ff52da",
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
              "id": "8fb0586f-5107-421a-becb-1dd4ef0b2bab"
            }
          ]
        },
        {
          "id": "54cfd179-133d-4a6a-b85a-743257e83150",
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
              "id": "75b3c7cd-33e9-41b8-bd69-52662da16780"
            }
          ]
        },
        {
          "id": "36ea26b4-c010-4a36-8af9-4c5aa3cdd5e8",
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
              "id": "0e22398d-e79f-4866-81aa-5fcf810d3465"
            }
          ]
        },
        {
          "id": "ba8208d0-cff9-4bb7-8190-eb44a9713701",
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
              "id": "bfe9de67-5b35-4c11-a462-31ae967d192d"
            }
          ]
        },
        {
          "id": "e3d48d32-22ea-4635-920c-b1cb1d17445c",
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
              "id": "7d7d201f-1311-4524-9c7e-4b72f1c8589f"
            }
          ]
        },
        {
          "id": "82d07d7b-9050-4731-930b-ba9e343d386b",
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
              "id": "f7cd4492-969d-40fa-aead-eda3ca68b77d"
            }
          ]
        },
        {
          "id": "a5a4de68-0a20-4abe-8dec-a7df58c485bc",
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
              "id": "5bd0d598-07a4-4599-9ad9-389173fa8c53"
            }
          ]
        }
      ]
    }
  ]
}
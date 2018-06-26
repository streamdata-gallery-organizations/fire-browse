{
  "info": {
    "name": "Fire Browse Beta API Retrieve links to summary reports from Firehose analysis runs.",
    "_postman_id": "0a2a026f-e30a-494b-98c2-ccca9adb76e5",
    "description": "This service returns URLs to the analysis result reports for runs of the Broad Institute GDAC Firehose analysis pipeline. At least one year of run reports are maintained in the database, but the reports from the latest run will be returned by default. The set of Nozzle reports returned may be filtered by disease cohort, report type and report name.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Analyses",
      "item": [
        {
          "id": "6b016d53-b454-4499-8e85-629fa38f5396",
          "name": "getAnalysesReports",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/Reports?cohort=%7B%7D&date=%7B%7D&format=%7B%7D&name=%7B%7D&page=%7B%7D&page_size=%7B%7D&sort_by=%7B%7D&type=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service returns URLs to the analysis result reports for runs of the Broad Institute GDAC Firehose analysis pipeline. At least one year of run reports are maintained in the database, but the reports from the latest run will be returned by default. The set of Nozzle reports returned may be filtered by disease cohort, report type and report name."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bb235e3f-5479-42c9-a27c-2ba965cb61dc"
            }
          ]
        }
      ]
    }
  ]
}
{
  "info": {
    "name": "Fire Browse Beta API Given a TCGA barcode, return its short letter sample type code.",
    "_postman_id": "bb551302-47bc-4075-8ad8-ab09dda6416f",
    "description": "Given a tcga barcode, return its short letter sample type code..",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Metadata",
      "item": [
        {
          "id": "c7685369-6e7f-47d9-bb63-899c97302b73",
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
              "id": "be8fd27d-2c57-4053-933c-fc2b2a6bb5f6"
            }
          ]
        }
      ]
    }
  ]
}
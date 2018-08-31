---
name: Fire Browse Beta API
x-slug: fire-browse-beta-api
description: A simple and elegant way to explore cancer data. Sitting above one of
  the deepest and most integratively characterized open cancer datasets in the world.
  Backed by a powerful computational infrastructure, application programming interface
  (API), graphical tools and online reports. With over 80K sample aliquots from 11,000+
  cancer patients, spanning 38 unique disease cohorts.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
x-kinRank: "7"
x-alexaRank: "0"
tags: Fire Browse Beta API
created: "2018-06-26"
modified: "2018-06-26"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/apis.md
specificationVersion: "0.14"
apis:
- name: Fire Browse Beta API Retrieve all data by genes Gistic2 results.
  x-api-slug: fire-browse-beta-api
  description: 'This service provides access to the Gistic2 all_data_by_genes.txt
    output data. This data is a gene-level table of copy number values for all samples.
    The returned copy number values are in units (copy number - 2) so that no amplification
    or deletion is 0, genes with amplifications have positive values, and genes with
    deletions are negative values. The data are converted from marker level to gene
    level using the extreme method: a gene is assigned the greatest amplification
    or the least deletion value among the markers it covers. Results may be filtered
    by cohort, gene, or barcode, but at least one gene or barcode must be supplied.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Analyses/CopyNumber/Genes/All
  tags: Analyses,CopyNumber,Genes
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysescopynumbergenesall-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysescopynumbergenesall-get-openapi.md
- name: Fire Browse Beta API Retrieve Gistic2 significantly amplified genes results.
  x-api-slug: fire-browse-beta-api
  description: This service provides access to the Gistic2 amp_genes.conf_99.txt output
    data.  At least 1 gene or cohort must be supplied.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Analyses/CopyNumber/Genes/Amplified
  tags: Analyses,CopyNumber,Genes,Amplified
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysescopynumbergenesamplified-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysescopynumbergenesamplified-get-openapi.md
- name: Fire Browse Beta API Retrieve Gistic2 significantly deleted genes results.
  x-api-slug: fire-browse-beta-api
  description: This service provides access to the Gistic2 del_genes.conf_99.txt output
    data.  At least 1 gene or cohort must be supplied.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Analyses/CopyNumber/Genes/Deleted
  tags: Analyses,CopyNumber,Genes,D
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysescopynumbergenesdeleted-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysescopynumbergenesdeleted-get-openapi.md
- name: Fire Browse Beta API Retrieve focal data by genes Gistic2 results.
  x-api-slug: fire-browse-beta-api
  description: 'This service provides access to the Gistic2 focal_data_by_genes.txt
    output data. This output is similar to the all_data_by_genes.txt output, but using
    only focal events with lengths greater than the  focal length cutoff. This data
    is a gene-level table of copy number values for all samples. The returned copy
    number values are in units (copy number - 2) so that no amplification or deletion
    is 0, genes with amplifications have positive values, and genes with deletions
    are negative values. The data are converted from marker level to gene level using
    the extreme method: a gene is assigned the greatest amplification or the least
    deletion value among the markers it covers. Results may be filtered by cohort,
    gene, and/or barcode, but at least one gene or barcode must be supplied.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Analyses/CopyNumber/Genes/Focal
  tags: Analyses,CopyNumber,Genes,Focal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysescopynumbergenesfocal-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysescopynumbergenesfocal-get-openapi.md
- name: Fire Browse Beta API Retrieve all thresholded by genes Gistic2 results.
  x-api-slug: fire-browse-beta-api
  description: 'This service provides access to the Gistic2 all_thresholded_by_genes.txt
    output data. A gene-level table of discrete amplification and deletion indicators
    for all samples. A table value of 0 means no amplification or deletion above the
    threshold. Amplifications are positive numbers: 1 means amplification above the
    amplification threshold; 2 means amplifications larger to the arm level amplifications
    observed for the sample. Deletions are represented by negative table values: -1
    represents deletion beyond the threshold; -2 means deletions greater than the
    minimum arm-level deletion observed for the sample. Results maybe filtered by
    cohort, gene or barcode, but at least one gene or barcode must be supplied.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Analyses/CopyNumber/Genes/Thresholded
  tags: Analyses,CopyNumber,Genes,Thresholded
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysescopynumbergenesthresholded-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysescopynumbergenesthresholded-get-openapi.md
- name: Fire Browse Beta API Retrieve aggregated analysis features table.
  x-api-slug: fire-browse-beta-api
  description: This service returns part or all of the so-called feature table; which
    aggregates the most important findings across ALL pipelines in the GDAC Firehose
    analysis workflow into a single table for simple access.  One feature table is
    created per disease cohort.  Results may be filtered by date or cohort, but at
    least 1 cohort must be specified here. For more details please visit the online
    documentation.  Please note that the service is still undergoing experimental
    evaluation and does not return JSON format.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Analyses/FeatureTable
  tags: Analyses,FeatureTable
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysesfeaturetable-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysesfeaturetable-get-openapi.md
- name: Fire Browse Beta API Retrieve MutSig final analysis MAF.
  x-api-slug: fire-browse-beta-api
  description: This service returns columns from the MAF generated by MutSig. Results
    may be filtered by gene, cohort, tool, or barcode, but at least one gene OR barcode
    OR cohort must be given.  By default a subset consisting of the most commonly
    used columns will be returned, but that can be modified with the column parameter.
    Specifying 'all' in this parameter is a convenient way to return every column
    of the respective MAF, and has precedence over any any other column selection
    expression.  The complete list of column names that may be specified is given
    here.  For more information on the mutation data, and how it is processed by Firehose,
    please consult the pipeline documentation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Analyses/Mutation/MAF
  tags: Analyses,Mutation,MAF
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysesmutationmaf-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysesmutationmaf-get-openapi.md
- name: Fire Browse Beta API Retrieve Significantly Mutated Genes (SMG).
  x-api-slug: fire-browse-beta-api
  description: This service provides a list of significantly mutated genes, as scored
    by MutSig.  It may be filtered by cohort, rank, gene, tool and/or Q-value threshold,
    but at least one cohort or gene must be supplied.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Analyses/Mutation/SMG
  tags: Analyses,Mutation,SMG
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysesmutationsmg-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysesmutationsmg-get-openapi.md
- name: Fire Browse Beta API Retrieve links to summary reports from Firehose analysis
    runs.
  x-api-slug: fire-browse-beta-api
  description: This service returns URLs to the analysis result reports for runs of
    the Broad Institute GDAC Firehose analysis pipeline. At least one year of run
    reports are maintained in the database, but the reports from the latest run will
    be returned by default. The set of Nozzle reports returned may be filtered by
    disease cohort, report type and report name.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Analyses/Reports
  tags: Analyses,Reports
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysesreports-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysesreports-get-openapi.md
- name: Fire Browse Beta API Returns RNASeq expression quartiles, e.g. suitable for
    drawing a boxplot.
  x-api-slug: fire-browse-beta-api
  description: For a given gene compute quartiles and extrema, suitable e.g. for drawing
    a boxplot (Tukey 1977).  Results may be filtered by cohort, sample type, patient
    barcode  or characterization protocol, and are returned sorted by cohort.  Note
    that samples for which no expression value was recorded (e.g. the melanoma sample
    TCGA-GN-262) are removed prior to calculation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Analyses/mRNASeq/Quartiles
  tags: Analyses,MRNASeq,Quartiles
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysesmrnaseqquartiles-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/analysesmrnaseqquartiles-get-openapi.md
- name: Fire Browse Beta API Retrieve standard data archives.
  x-api-slug: fire-browse-beta-api
  description: This service returns the archive URLs for our Firehose standard data
    runs, providing a RESTful interface similar in spirit to the command line firehose_get
    tool. The archives can be filtered based on date, cohort, data type, platform,
    center, data level, and protocol.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Archives/StandardData
  tags: Archives,StandardData
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/archivesstandarddata-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/archivesstandarddata-get-openapi.md
- name: Fire Browse Beta API Obtain identities of TCGA consortium member centers.
  x-api-slug: fire-browse-beta-api
  description: By default this function returns a table of all consortium members
    in TCGA, aka centers; it provides both the HTTP domain and full organizational
    name of each center.  A subset of this table may be obtained by explicitly specifying
    one or more domain names.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Metadata/Centers
  tags: Metadata,Centers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatacenters-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatacenters-get-openapi.md
- name: Fire Browse Beta API Retrieve names of all TCGA clinical data elements (CDEs).
  x-api-slug: fire-browse-beta-api
  description: Retrieve names of all patient-level clinical data elements (CDES) available
    in TCGA, unioned across all disease cohorts. A CDE will be listed here only when
    it has a value other than NA for at least 1 patient case in any disease cohort.
    For more information on how these CDEs are processed see our pipeline documentation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Metadata/ClinicalNames
  tags: Metadata,ClinicalNames
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadataclinicalnames-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadataclinicalnames-get-openapi.md
- name: Fire Browse Beta API Retrieve names of CDEs normalized by Firehose and selected
    for analyses.
  x-api-slug: fire-browse-beta-api
  description: This service returns the names of patient-level clinical data elements
    (CDEs) that have been normalized by Firehose for use in analyses, unioned across
    all disease cohorts. For more information on how these CDEs are processed, see
    our pipeline documentation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Metadata/ClinicalNames_FH
  tags: Metadata,ClinicalNames,FH
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadataclinicalnames-fh-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadataclinicalnames-fh-get-openapi.md
- name: Fire Browse Beta API Translate TCGA cohort abbreviations to full disease names.
  x-api-slug: fire-browse-beta-api
  description: By default this function returns a table containing all TCGA cohort
    abbreviations and their corresponding disease names.  A subset of that table may
    be obtained by explicitly specifying one or more cohort abbreviations.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Metadata/Cohorts
  tags: Metadata,Cohorts
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatacohorts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatacohorts-get-openapi.md
- name: Fire Browse Beta API Retrieve sample counts.
  x-api-slug: fire-browse-beta-api
  description: |-
    Returns the aliquot counts for each disease cohort, per sample
    type and data type.  The sample type designation of "Tumor"
    may be used to aggregate the count of all tumor aliquots into
    a single number per disease and data type. See the SampleTypes
    function for a complete description of sample types.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Metadata/Counts
  tags: Metadata,Counts
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatacounts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatacounts-get-openapi.md
- name: Fire Browse Beta API Retrieve datestamps of all GDAC Firehose standard data
    and analyses runs that have been ingested into FireBrowse.
  x-api-slug: fire-browse-beta-api
  description: Retrieve datestamps of all gdac firehose standard data and analyses
    runs that have been ingested into firebrowse..
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Metadata/Dates
  tags: Metadata,Dates
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatadates-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatadates-get-openapi.md
- name: Fire Browse Beta API Simple way to discern whether API server is up and running
  x-api-slug: fire-browse-beta-api
  description: Returns a message to indicate that API (server) is up and running,
    or times out if not.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Metadata/HeartBeat
  tags: Metadata,HeartBeat
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadataheartbeat-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadataheartbeat-get-openapi.md
- name: Fire Browse Beta API Retrieve names of all columns in the mutation annotation
    files (MAFs) served by FireBrowse.
  x-api-slug: fire-browse-beta-api
  description: Retrieve the names of all columns in the mutation annotation files
    (MAFs) hosted by FireBrowse.  For more information on the mutation data, and how
    it is processed by Firehose, please consult the pipeline documentation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Metadata/MAFColNames
  tags: Metadata,MAFColNames
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatamafcolnames-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatamafcolnames-get-openapi.md
- name: Fire Browse Beta API Retrieve list of all TCGA patients.
  x-api-slug: fire-browse-beta-api
  description: This service returns a list of all TCGA patient barcodes in FireBrowse,
    optionally filtered by disease cohort.  The barcodes are obtained directy from
    the clinical data.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Metadata/Patients
  tags: Metadata,Patients
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatapatients-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatapatients-get-openapi.md
- name: Fire Browse Beta API Translate TCGA platform codes to full platform names.
  x-api-slug: fire-browse-beta-api
  description: By default this function returns a table of all of the technology platforms
    used to sequence or characterize samples in TCGA--both their short platform codes
    and full names.  A subset of this table may be obtained by explicitly specifying
    one or more platform codes.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Metadata/Platforms
  tags: Metadata,Platforms
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadataplatforms-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadataplatforms-get-openapi.md
- name: Fire Browse Beta API Given a TCGA barcode, return its short letter sample
    type code.
  x-api-slug: fire-browse-beta-api
  description: Given a tcga barcode, return its short letter sample type code..
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Metadata/SampleType/Barcode/{TCGA_Barcode}
  tags: Metadata,SampleType,Barcode,TCGA,Barcode
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatasampletypebarcodetcga-barcode-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatasampletypebarcodetcga-barcode-get-openapi.md
- name: Fire Browse Beta API Translate from numeric to symbolic TCGA sample codes.
  x-api-slug: fire-browse-beta-api
  description: Convert a TCGA numeric sample type code (e.g. 01, 02) to its corresponding
    symbolic (short letter) code (e.g. TP, TR).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Metadata/SampleType/Code/{code}
  tags: Metadata,SampleType,Code,Code
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatasampletypecodecode-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatasampletypecodecode-get-openapi.md
- name: Fire Browse Beta API Translate from symbolic to numeric TCGA sample codes.
  x-api-slug: fire-browse-beta-api
  description: Convert a TCGA sample type code in symbolic form (or 'short letter
    code' like TP, TR) to its corresponding numeric form (e.g. 01, 02).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Metadata/SampleType/ShortLetterCode/{short_letter_code}
  tags: Metadata,SampleType,ShortLetterCode,Short,Letter,Code
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatasampletypeshortlettercodeshort-letter-code-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatasampletypeshortlettercodeshort-letter-code-get-openapi.md
- name: Fire Browse Beta API Return all TCGA sample type codes, both numeric and symbolic.
  x-api-slug: fire-browse-beta-api
  description: Return all tcga sample type codes, both numeric and symbolic..
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Metadata/SampleTypes
  tags: Metadata,SampleTypes
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatasampletypes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatasampletypes-get-openapi.md
- name: Fire Browse Beta API Obtain identities of tissue source sites in TCGA.
  x-api-slug: fire-browse-beta-api
  description: By default this function returns a table of all sites which contributed
    source tissue to TCGA, aka TSS's. A subset of this table may be obtained by explicitly
    specifying one or more sites.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Metadata/TSSites
  tags: Metadata,TSSites
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatatssites-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/metadatatssites-get-openapi.md
- name: Fire Browse Beta API Retrieve TCGA CDEs verbatim, i.e. not normalized by Firehose.
  x-api-slug: fire-browse-beta-api
  description: This service returns patient clinical data from TCGA, verbatim. It
    differs from the Samples/Clinical_FH method by providing access to all TCGA CDEs
    in their original form, not merely the subset of CDEs normalized by Firehose for
    analyses.  Results may be selected by disease cohort, patient barcode or CDE name,
    but at least one cohort, barcode, or CDE must be provided. When filtering by CDE
    note that only when a patient record contains one or more of the selected CDEs
    will it be returned. Visit the Metadata/ClinicalNames api function to see the
    entire list of TCGA CDEs that may be queried via this method. For more information
    on how clinical data are processed, see our pipeline documentation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Samples/Clinical
  tags: Samples,Clinical
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/samplesclinical-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/samplesclinical-get-openapi.md
- name: Fire Browse Beta API Retrieve CDEs normalized by Firehose and selected for
    analyses.
  x-api-slug: fire-browse-beta-api
  description: This service returns patient-level clinical data elements (CDEs) that
    have been normalized by Firehose for use in analyses. Results may be selected
    by disease cohort, patient barcode or CDE name, but at least one cohort, barcode
    or CDE must be provided. When filtering by CDE note that only when a  patient
    record contains one or more of the selected CDEs will it be returned. Visit this
    table of CDEs to see what's available for every disase cohort; for more information
    on how these CDEs are processed see our pipeline documentation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Samples/Clinical_FH
  tags: Samples,Clinical,FH
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/samplesclinical-fh-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/samplesclinical-fh-get-openapi.md
- name: Fire Browse Beta API Retrieve mRNASeq data.
  x-api-slug: fire-browse-beta-api
  description: This service returns sample-level log2 mRNASeq expression values. Results
    may be filtered by gene, cohort, barcode, sample type or characterization protocol,
    but at least one gene must be supplied.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Samples/mRNASeq
  tags: Samples,MRNASeq
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/samplesmrnaseq-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/samplesmrnaseq-get-openapi.md
- name: Fire Browse Beta API Retrieve miRSeq data.
  x-api-slug: fire-browse-beta-api
  description: This service returns sample-level log2 miRSeq expression values. Results
    may be filtered by miR, cohort, barcode, sample type or Firehose preprocessing
    tool, but at least one miR must be supplied.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Samples/miRSeq
  tags: Samples,MiRSeq
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/samplesmirseq-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/samplesmirseq-get-openapi.md
- name: Fire Browse Beta API
  x-api-slug: fire-browse-beta-api
  description: A simple and elegant way to explore cancer data. Sitting above one
    of the deepest and most integratively characterized open cancer datasets in the
    world. Backed by a powerful computational infrastructure, application programming
    interface (API), graphical tools and online reports. With over 80K sample aliquots
    from 11,000+ cancer patients, spanning 38 unique disease cohorts.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1
  tags: Fire Browse Beta API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/fire-browse-beta-api/master/_listings/fire-browse-beta-api/openapi.md
x-common:
- type: x-website
  url: http://firebrowse.org
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---
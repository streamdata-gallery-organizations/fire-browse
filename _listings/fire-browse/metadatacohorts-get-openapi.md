---
swagger: "2.0"
x-collection-name: Fire Browse
x-complete: 0
info:
  title: Fire Browse Beta API Translate TCGA cohort abbreviations to full disease
    names.
  description: By default this function returns a table containing all TCGA cohort
    abbreviations and their corresponding disease names.  A subset of that table may
    be obtained by explicitly specifying one or more cohort abbreviations.
  version: 1.1.35 (2016-09-27 10:12:23 6a47e74011281b2aa
host: firebrowse.org
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Analyses/CopyNumber/Genes/All:
    get:
      summary: Retrieve all data by genes Gistic2 results.
      description: 'This service provides access to the Gistic2 all_data_by_genes.txt
        output data. This data is a gene-level table of copy number values for all
        samples. The returned copy number values are in units (copy number - 2) so
        that no amplification or deletion is 0, genes with amplifications have positive
        values, and genes with deletions are negative values. The data are converted
        from marker level to gene level using the extreme method: a gene is assigned
        the greatest amplification or the least deletion value among the markers it
        covers. Results may be filtered by cohort, gene, or barcode, but at least
        one gene or barcode must be supplied.'
      operationId: getAnalysesCopynumberGenesAll
      x-api-path-slug: analysescopynumbergenesall-get
      parameters:
      - in: query
        name: cohort
        description: Narrow search to one or more TCGA disease cohorts from the scrollable
          list
      - in: query
        name: format
        description: Format of result
      - in: query
        name: gene
        description: Comma separated list of gene name(s)
      - in: query
        name: page
        description: Which page (slice) of entire results set should be returned
      - in: query
        name: page_size
        description: Number of records per page of results
      - in: query
        name: sort_by
        description: Which column in the results should be used for sorting paginated
          results?
      - in: query
        name: tcga_participant_barcode
        description: Comma separated list of TCGA participant barcodes (e
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - CopyNumber
      - Genes
  /Analyses/CopyNumber/Genes/Amplified:
    get:
      summary: Retrieve Gistic2 significantly amplified genes results.
      description: This service provides access to the Gistic2 amp_genes.conf_99.txt
        output data.  At least 1 gene or cohort must be supplied.
      operationId: getAnalysesCopynumberGenesAmplified
      x-api-path-slug: analysescopynumbergenesamplified-get
      parameters:
      - in: query
        name: cohort
        description: Narrow search to one or more TCGA disease cohorts from the scrollable
          list
      - in: query
        name: format
        description: Format of result
      - in: query
        name: gene
        description: Comma separated list of gene name(s)
      - in: query
        name: page
        description: Which page (slice) of entire results set should be returned
      - in: query
        name: page_size
        description: Number of records per page of results
      - in: query
        name: q
        description: Only return results with Q-value
      - in: query
        name: sort_by
        description: Which column in the results should be used for sorting paginated
          results?
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - CopyNumber
      - Genes
      - Amplified
  /Analyses/CopyNumber/Genes/Deleted:
    get:
      summary: Retrieve Gistic2 significantly deleted genes results.
      description: This service provides access to the Gistic2 del_genes.conf_99.txt
        output data.  At least 1 gene or cohort must be supplied.
      operationId: getAnalysesCopynumberGenesDeleted
      x-api-path-slug: analysescopynumbergenesdeleted-get
      parameters:
      - in: query
        name: cohort
        description: Narrow search to one or more TCGA disease cohorts from the scrollable
          list
      - in: query
        name: format
        description: Format of result
      - in: query
        name: gene
        description: Comma separated list of gene name(s)
      - in: query
        name: page
        description: Which page (slice) of entire results set should be returned
      - in: query
        name: page_size
        description: Number of records per page of results
      - in: query
        name: q
        description: Only return results with Q-value
      - in: query
        name: sort_by
        description: Which column in the results should be used for sorting paginated
          results?
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - CopyNumber
      - Genes
      - D
  /Analyses/CopyNumber/Genes/Focal:
    get:
      summary: Retrieve focal data by genes Gistic2 results.
      description: 'This service provides access to the Gistic2 focal_data_by_genes.txt
        output data. This output is similar to the all_data_by_genes.txt output, but
        using only focal events with lengths greater than the  focal length cutoff.
        This data is a gene-level table of copy number values for all samples. The
        returned copy number values are in units (copy number - 2) so that no amplification
        or deletion is 0, genes with amplifications have positive values, and genes
        with deletions are negative values. The data are converted from marker level
        to gene level using the extreme method: a gene is assigned the greatest amplification
        or the least deletion value among the markers it covers. Results may be filtered
        by cohort, gene, and/or barcode, but at least one gene or barcode must be
        supplied.'
      operationId: getAnalysesCopynumberGenesFocal
      x-api-path-slug: analysescopynumbergenesfocal-get
      parameters:
      - in: query
        name: cohort
        description: Narrow search to one or more TCGA disease cohorts from the scrollable
          list
      - in: query
        name: format
        description: Format of result
      - in: query
        name: gene
        description: Comma separated list of gene name(s)
      - in: query
        name: page
        description: Which page (slice) of entire results set should be returned
      - in: query
        name: page_size
        description: Number of records per page of results
      - in: query
        name: sort_by
        description: Which column in the results should be used for sorting paginated
          results?
      - in: query
        name: tcga_participant_barcode
        description: Comma separated list of TCGA participant barcodes (e
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - CopyNumber
      - Genes
      - Focal
  /Analyses/CopyNumber/Genes/Thresholded:
    get:
      summary: Retrieve all thresholded by genes Gistic2 results.
      description: 'This service provides access to the Gistic2 all_thresholded_by_genes.txt
        output data. A gene-level table of discrete amplification and deletion indicators
        for all samples. A table value of 0 means no amplification or deletion above
        the threshold. Amplifications are positive numbers: 1 means amplification
        above the amplification threshold; 2 means amplifications larger to the arm
        level amplifications observed for the sample. Deletions are represented by
        negative table values: -1 represents deletion beyond the threshold; -2 means
        deletions greater than the minimum arm-level deletion observed for the sample.
        Results maybe filtered by cohort, gene or barcode, but at least one gene or
        barcode must be supplied.'
      operationId: getAnalysesCopynumberGenesThresholded
      x-api-path-slug: analysescopynumbergenesthresholded-get
      parameters:
      - in: query
        name: cohort
        description: Narrow search to one or more TCGA disease cohorts from the scrollable
          list
      - in: query
        name: format
        description: Format of result
      - in: query
        name: gene
        description: Comma separated list of gene name(s)
      - in: query
        name: page
        description: Which page (slice) of entire results set should be returned
      - in: query
        name: page_size
        description: Number of records per page of results
      - in: query
        name: sort_by
        description: Which column in the results should be used for sorting paginated
          results?
      - in: query
        name: tcga_participant_barcode
        description: Comma separated list of TCGA participant barcodes (e
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - CopyNumber
      - Genes
      - Thresholded
  /Analyses/FeatureTable:
    get:
      summary: Retrieve aggregated analysis features table.
      description: This service returns part or all of the so-called feature table;
        which aggregates the most important findings across ALL pipelines in the GDAC
        Firehose analysis workflow into a single table for simple access.  One feature
        table is created per disease cohort.  Results may be filtered by date or cohort,
        but at least 1 cohort must be specified here. For more details please visit
        the online documentation.  Please note that the service is still undergoing
        experimental evaluation and does not return JSON format.
      operationId: getAnalysesFeaturetable
      x-api-path-slug: analysesfeaturetable-get
      parameters:
      - in: query
        name: cohort
        description: Narrow search to one or more TCGA disease cohorts from the scrollable
          list
      - in: query
        name: column
        description: Comma separated list of which data columns/fields to return
      - in: query
        name: date
        description: Select one or more date stamps
      - in: query
        name: format
        description: Format of result
      - in: query
        name: page
        description: Which page (slice) of entire results set should be returned
      - in: query
        name: page_size
        description: Number of records per page of results
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - FeatureTable
  /Analyses/Mutation/MAF:
    get:
      summary: Retrieve MutSig final analysis MAF.
      description: This service returns columns from the MAF generated by MutSig.
        Results may be filtered by gene, cohort, tool, or barcode, but at least one
        gene OR barcode OR cohort must be given.  By default a subset consisting of
        the most commonly used columns will be returned, but that can be modified
        with the column parameter. Specifying 'all' in this parameter is a convenient
        way to return every column of the respective MAF, and has precedence over
        any any other column selection expression.  The complete list of column names
        that may be specified is given here.  For more information on the mutation
        data, and how it is processed by Firehose, please consult the pipeline documentation.
      operationId: getAnalysesMutationMaf
      x-api-path-slug: analysesmutationmaf-get
      parameters:
      - in: query
        name: cohort
        description: Narrow search to one or more TCGA disease cohorts from the scrollable
          list
      - in: query
        name: column
        description: Comma separated list of which data columns/fields to return
      - in: query
        name: format
        description: Format of result
      - in: query
        name: gene
        description: Comma separated list of gene name(s)
      - in: query
        name: page
        description: Which page (slice) of entire results set should be returned
      - in: query
        name: page_size
        description: Number of records per page of results
      - in: query
        name: sort_by
        description: Which column in the results should be used for sorting paginated
          results?
      - in: query
        name: tcga_participant_barcode
        description: Comma separated list of TCGA participant barcodes (e
      - in: query
        name: tool
        description: Narrow search to include only data/results produced by the selected
          Firehose tool
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Mutation
      - MAF
  /Analyses/Mutation/SMG:
    get:
      summary: Retrieve Significantly Mutated Genes (SMG).
      description: This service provides a list of significantly mutated genes, as
        scored by MutSig.  It may be filtered by cohort, rank, gene, tool and/or Q-value
        threshold, but at least one cohort or gene must be supplied.
      operationId: getAnalysesMutationSmg
      x-api-path-slug: analysesmutationsmg-get
      parameters:
      - in: query
        name: cohort
        description: Narrow search to one or more TCGA disease cohorts from the scrollable
          list
      - in: query
        name: format
        description: Format of result
      - in: query
        name: gene
        description: Comma separated list of gene name(s)
      - in: query
        name: page
        description: Which page (slice) of entire results set should be returned
      - in: query
        name: page_size
        description: Number of records per page of results
      - in: query
        name: q
        description: Only return results with Q-value
      - in: query
        name: rank
        description: Number of significant genes to return
      - in: query
        name: sort_by
        description: Which column in the results should be used for sorting paginated
          results?
      - in: query
        name: tool
        description: Narrow search to include only data/results produced by the selected
          Firehose tool
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Mutation
      - SMG
  /Analyses/Reports:
    get:
      summary: Retrieve links to summary reports from Firehose analysis runs.
      description: This service returns URLs to the analysis result reports for runs
        of the Broad Institute GDAC Firehose analysis pipeline. At least one year
        of run reports are maintained in the database, but the reports from the latest
        run will be returned by default. The set of Nozzle reports returned may be
        filtered by disease cohort, report type and report name.
      operationId: getAnalysesReports
      x-api-path-slug: analysesreports-get
      parameters:
      - in: query
        name: cohort
        description: Narrow search to one or more TCGA disease cohorts from the scrollable
          list
      - in: query
        name: date
        description: Select one or more date stamps
      - in: query
        name: format
        description: Format of result
      - in: query
        name: name
        description: Narrow search to one or more report names
      - in: query
        name: page
        description: Which page (slice) of entire results set should be returned
      - in: query
        name: page_size
        description: Number of records per page of results
      - in: query
        name: sort_by
        description: Which column in the results should be used for sorting paginated
          results?
      - in: query
        name: type
        description: Narrow search to one or more report types
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Reports
  /Analyses/mRNASeq/Quartiles:
    get:
      summary: Returns RNASeq expression quartiles, e.g. suitable for drawing a boxplot.
      description: For a given gene compute quartiles and extrema, suitable e.g. for
        drawing a boxplot (Tukey 1977).  Results may be filtered by cohort, sample
        type, patient barcode  or characterization protocol, and are returned sorted
        by cohort.  Note that samples for which no expression value was recorded (e.g.
        the melanoma sample TCGA-GN-262) are removed prior to calculation.
      operationId: getAnalysesMrnaseqQuartiles
      x-api-path-slug: analysesmrnaseqquartiles-get
      parameters:
      - in: query
        name: cohort
        description: Narrow search to one or more TCGA disease cohorts from the scrollable
          list
      - in: query
        name: Exclude
        description: Comma separated list of TCGA participants, identified by barcodes
          such as TCGA-GF-A4EO, denoting samples to exclude from computation
      - in: query
        name: format
        description: Format of result
      - in: query
        name: gene
        description: Enter a single gene name
      - in: query
        name: protocol
        description: Narrow search to one or more sample characterization protocols
          from the scrollable list
      - in: query
        name: sample_type
        description: For which type of sample(s) should quartiles be computed?
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - MRNASeq
      - Quartiles
  /Archives/StandardData:
    get:
      summary: Retrieve standard data archives.
      description: This service returns the archive URLs for our Firehose standard
        data runs, providing a RESTful interface similar in spirit to the command
        line firehose_get tool. The archives can be filtered based on date, cohort,
        data type, platform, center, data level, and protocol.
      operationId: getArchivesStandarddata
      x-api-path-slug: archivesstandarddata-get
      parameters:
      - in: query
        name: center
        description: Narrow search to one or more TCGA centers from the scrollable
          list
      - in: query
        name: cohort
        description: Narrow search to one or more TCGA disease cohorts from the scrollable
          list
      - in: query
        name: data_type
        description: Narrow search to one or more TCGA data types from the scrollable
          list
      - in: query
        name: date
        description: Select one or more date stamps
      - in: query
        name: format
        description: Format of result
      - in: query
        name: level
        description: Narrow search to one or more TCGA data levels
      - in: query
        name: page
        description: Which page (slice) of entire results set should be returned
      - in: query
        name: page_size
        description: Number of records per page of results
      - in: query
        name: platform
        description: Narrow search to one or more TCGA data generation platforms from
          the scrollable list
      - in: query
        name: protocol
        description: Narrow search to one or more sample characterization protocols
          from the scrollable list
      - in: query
        name: sort_by
        description: Which column in the results should be used for sorting paginated
          results?
      - in: query
        name: tool
        description: Narrow search to include only data/results produced by the selected
          Firehose tool
      responses:
        200:
          description: OK
      tags:
      - Archives
      - StandardData
  /Metadata/Centers:
    get:
      summary: Obtain identities of TCGA consortium member centers.
      description: By default this function returns a table of all consortium members
        in TCGA, aka centers; it provides both the HTTP domain and full organizational
        name of each center.  A subset of this table may be obtained by explicitly
        specifying one or more domain names.
      operationId: getMetadataCenters
      x-api-path-slug: metadatacenters-get
      parameters:
      - in: query
        name: center
        description: Narrow search to one or more TCGA centers from the scrollable
          list
      - in: query
        name: format
        description: Format of result
      responses:
        200:
          description: OK
      tags:
      - Metadata
      - Centers
  /Metadata/ClinicalNames:
    get:
      summary: Retrieve names of all TCGA clinical data elements (CDEs).
      description: Retrieve names of all patient-level clinical data elements (CDES)
        available in TCGA, unioned across all disease cohorts. A CDE will be listed
        here only when it has a value other than NA for at least 1 patient case in
        any disease cohort. For more information on how these CDEs are processed see
        our pipeline documentation.
      operationId: getMetadataClinicalnames
      x-api-path-slug: metadataclinicalnames-get
      parameters:
      - in: query
        name: format
        description: Format of result
      responses:
        200:
          description: OK
      tags:
      - Metadata
      - ClinicalNames
  /Metadata/ClinicalNames_FH:
    get:
      summary: Retrieve names of CDEs normalized by Firehose and selected for analyses.
      description: This service returns the names of patient-level clinical data elements
        (CDEs) that have been normalized by Firehose for use in analyses, unioned
        across all disease cohorts. For more information on how these CDEs are processed,
        see our pipeline documentation.
      operationId: getMetadataClinicalnamesFh
      x-api-path-slug: metadataclinicalnames-fh-get
      parameters:
      - in: query
        name: format
        description: Format of result
      responses:
        200:
          description: OK
      tags:
      - Metadata
      - ClinicalNames
      - FH
  /Metadata/Cohorts:
    get:
      summary: Translate TCGA cohort abbreviations to full disease names.
      description: By default this function returns a table containing all TCGA cohort
        abbreviations and their corresponding disease names.  A subset of that table
        may be obtained by explicitly specifying one or more cohort abbreviations.
      operationId: getMetadataCohorts
      x-api-path-slug: metadatacohorts-get
      parameters:
      - in: query
        name: cohort
        description: Narrow search to one or more TCGA disease cohorts from the scrollable
          list
      - in: query
        name: format
        description: Format of result
      responses:
        200:
          description: OK
      tags:
      - Metadata
      - Cohorts
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---
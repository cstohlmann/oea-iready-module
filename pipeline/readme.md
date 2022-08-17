# Pipelines

This module uses a Synapse pipeline to:
1. Land iReady Diagnostic and Instruction Assessment data (either test or production data) into Stage 1np.
2. Process data into Stages 2np and 2p.
3. Create a SQL database to query Stage 2np and 2p data via Power BI.

<strong><em>[CHANGE ALL PICTURES AND MOST LINKS]</strong></em>

Module Pipeline for Test Data  | Module Pipeline for Production Data
:-------------------------:|:-------------------------:
![](https://github.com/cviddenKwantum/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/pipeline%20overview.png) |  ![](https://github.com/cviddenKwantum/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/pipeline%20overview%20prod.png)  

For production data, this module pipeline can be automated triggered (i.e. daily or weekly) to keep your Synapse data lake up-to-date.

## Pipeline Setup Instructions

Two sets of instructions are included:
1. [Test data pipeline instructions](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/iReady/pipeline#test-data-pipeline-instructions)
2. [Production data pipeline instructions](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/iReady/pipeline#production-data-pipeline-instructions)

### Test Data Pipeline Instructions

1. Complete the first steps of the [iReady module setup instructions](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/iReady#module-setup-instructions)
2. Download the [iReady pipeline template](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/iReady/pipeline/iready_pipeline_template.zip) locally to your computer.
3. Import the pipeline template to your Synapse workspace.
<img src="https://github.com/cstohlmann/oea-iready-module/blob/main/docs/images/Test%20Data%20Pipeline%20Instructions_1.png" width="600">
4. Assign the Synapse linked services needed to support the pipeline template.
<img src="https://github.com/cstohlmann/oea-iready-module/blob/main/docs/images/Test%20Data%20Pipeline%20Instructions_2.png" width="600">
5. Change the iReady_pipeline_template storageAccount parameter to be your storage account name.
<img src="https://github.com/cstohlmann/oea-iready-module/blob/main/docs/images/Test%20Data%20Pipeline%20Instructions_3.png" width="600">
6. Select a spark pool for the ingest_into_stage2p_and_2np notebook.
<img src="https://github.com/cstohlmann/oea-iready-module/blob/main/docs/images/Test%20Data%20Pipeline%20Instructions_4.png" width="600">
7. Trigger the pipeline mannually.
<img src="https://github.com/cviddenKwantum/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/pipeline%20trigger.png" width="600">
8. Once the pipeline has successfully executed, verify that:

- Data has landed in Stage 1np
<img src="https://github.com/cviddenKwantum/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/pipeline%20land%20stage1.png" width="600">
- Data has been processed to Stages 2p and 2np
<img src="https://github.com/cviddenKwantum/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/pipeline%20stage2p.png" width="600">
<img src="https://github.com/cviddenKwantum/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/pipeline%20stage2np.png" width="600">
- SQL database has been created
<img src="https://github.com/cviddenKwantum/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/pipeline%20sql.png" width="600">

### Production Data Pipeline Instructions

<strong><em>[THIS SECTION NEEDS TO BE COMPLETELY RE-WORKED]</strong></em>

1. Complete the [Test Data Pipeline Instructions](https://github.com/cviddenKwantum/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/Clever/pipeline#test-data-pipeline-instructions), but do not execute the pipeline yet.
2. Review the Clever Participation Report [instructions for exporting reports](https://support.clever.com/hc/s/articles/360049642311?language=en_US#ExportingReports).
3. Create a [SFTP Synapse linked service](https://docs.microsoft.com/en-us/azure/data-factory/connector-sftp?tabs=data-factory#linked-service-properties).
<img src="https://github.com/cviddenKwantum/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/pipeline%20prod%20linked%20service.png" width="600">
4. Download the iReady module pipeline template for the [production data ingestion](https://github.com/cviddenKwantum/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/pipeline/Extracts) and import into your Synapse workspace. You will see a new sub-pipeline added to the pipeline Extracts folder.
<img src="https://github.com/cviddenKwantum/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/pipeline%20prod%20land.png" width="600">
5. Open the iready_main_pipeline. Delete the initial iready_copy_test_data subpipeline and replace with the iready_data_ingestion pipeline. The final results is shown below.
<img src="https://github.com/cviddenKwantum/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/pipeline%20overview%20prod.png" width="600">
6. Trigger the pipeline mannually.
<img src="https://github.com/cviddenKwantum/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/pipeline%20trigger.png" width="600">
7. Once the pipeline has successfully executed, verify that:

- Data has landed in Stage 1np
<img src="https://github.com/cviddenKwantum/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/pipeline%20land%20stage1.png" width="600">
- Data has been processed to Stages 2p and 2np
<img src="https://github.com/cviddenKwantum/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/pipeline%20stage2p.png" width="600">
<img src="https://github.com/cviddenKwantum/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/pipeline%20stage2np.png" width="600">
- SQL database has been created
<img src="https://github.com/cviddenKwantum/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/pipeline%20sql.png" width="600">





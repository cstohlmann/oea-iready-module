# iReady Module

<strong><em>[THIS SECTION NEEDS UPDATING]</strong></em>

[iReady](https://www.curriculumassociates.com/programs/i-ready-assessment) offers a variety of assessments for K-12 students, which tracks learning progress in reading and mathematics. This iReady OEA module, <strong><em>[SHOULD WE INCLUDE THIS HERE?]</strong></em> developed by the [Fresno Unified School District](https://www.fresnounified.org/) in Fresno, California USA, provides students learning progress data and subsequent breakdowns of assessment material and scores. Data is retrieved through <strong><em>[INSERT HERE]()</strong></em> which can be either manually downloaded or [automated via SFTP delivery](). iReady Assessment Reports data will enable education leaders to see the impact of certain pedagogies/teaching-styles on student learning. 

## Problem Statement and Module Impact

Collecting data related to student learning progress and results is critical in evaluating the success and areas-of-growth for teachers. As learning styles are increasingly changing, understanding the impact of various resources students use is fundamental to supporting student success.

This iReady OEA module will aid K-12 education systems in bringing student learning progress data to their Azure data lake for analysis. The [module Synapse pipeline](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/iReady/pipeline) will connect to on-premises servers by pulling csv files from assessment reports, to process the data so that this data is standardized and queryable. The [module Power BI template](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/iReady/powerbi) allows users to immediately explore the data and start developing custom dashboards enabling education systems to better understand the trends in student learning progress. 

## Module Setup Instructions

1. Ensure you have proper [Azure subscription and credentials](https://github.com/microsoft/OpenEduAnalytics#what-you-need).
2. Setup the [most recent version of OEA](https://github.com/microsoft/OpenEduAnalytics#setup). This will include the most recent version of the [OEA python class](https://github.com/microsoft/OpenEduAnalytics/blob/main/framework/notebook/OEA_py.ipynb).
3. Import the [iReady module class notebook](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/iReady/notebook/iReady_py.ipynb) into your Synapse workspace. This notebook contains data schema information and data writing functions needed to support module pipelines. 
4. Import the [iReady pipeline template](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/iReady/pipeline) into your Synapse workspace and execute the pipeline. See the [module pipeline page](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/iReady/pipeline) for detailed instructions.
5. Verify that the module pipeline landed data into stage 1 and 2 and SQL databases were created. See the [module pipeline page](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/iReady/pipeline) for detailed instructions.
6. Download the [module Power BI template file](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/iReady/powerbi). Module test data is already imported into the Power BI. See the [module Power BI page](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/iReady/powerbi) page for instructions for switching the Power BI template data source to import from your Synapse workspace data source.

#### Note: 
The above instructions will setup the iReady OEA module using the [module test data](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/iReady/test_data), but the same pipeline can be used for production data. See the [module pipeline page](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/iReady/pipeline) for instructions on switching the pipeline data source to production data.

## Data Sources

<strong><em>[LINKS IN THIS SECTION + DESCRIPTIONS NEED TO BE UPDATED]</strong></em>

This module imports data which matches the format of the eight [iReady Assessment Reports]().
- [Daily Participation Report](https://support.clever.com/hc/s/articles/360049642311?language=en_US#step2) Participation reports provide a daily snapshot that summarizes usage for students, teachers, and staff in your district, including those that may be inactive. 
- [Resource Usage Report](https://support.clever.com/hc/s/articles/360049642311?language=en_US#h_7698d144-7ceb-4d63-88b8-e9ca2aa378d2) provide a daily snapshot of each resource accessed by a user on a given day and are available for active students, teachers, and staff. 

See the [module test data page](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/iReady/test_data) for details on data format and contents.

## Module Components

<strong><em>[LINKS IN THIS SECTION NEED TO BE UPDATED]</strong></em>

Out-of-the box assets for this OEA module include: 
1. [Test Data](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/iReady/test_data): Artificially generated test data which supports the module pipeline and Power BI template. Test data matches the [iReady Diagnostic and Personalized Instruction Assessment Reports]() format exactly.
2. [Pipeline Template](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/iReady/pipeline): One main pipeline template which lands data into Stage 1 and processes into Stage 2. Stage 2 data is then made available via a serveless SQL endpoint.
    - <strong><em>[INCLUDE DESCRIPTION OF PRODUCTION-LEVEL DATA INGESTION SUB-PIPELINE??]</strong></em>
3. [Notebooks](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/iReady/notebook): 
    - [iReady_py.ipynb](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/iReady/notebook/iReady_py.ipynb): A module python class notebook that defines the data schemas and basic functions of data ingestion and processing from Stage 1 to Stage 2.
    - [iReady_module_ingestion.ipynb](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/iReady/notebook/iReady_module_ingestion.ipynb): Module data ingestion notebook which depends on the the module class. The pipeline template automatically uploads this notebook upon importing. 
4. [PowerBI template](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/iReady/powerbi): A Power BI template which explores data in a basic way. The Power BI file is pre-loaded with test data making it easy to quickly interact with iReady data. See instructions on the [module PowerBI page](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Digital_Learning_Apps_and_Platforms/iReady/powerbi) to switch the dashboard data source to direct query from your Synapse workspace. Screenshots of the Power BI template are below.

<strong><em>[PICTURES NEED TO BE UPDATED]</strong></em>

Dashboard Explanation  | Dashboard Usage Summary
:-------------------------:|:-------------------------:
![](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/Clever%20Module%20Explanation%20Page.png) |  ![](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/Clever%20Module%20Dashboard%20Sample.png)  

## Additional Information

<strong><em>[MAY WANT TO UPDATE, OTHERWISE REMOVE]</strong></em>

While this module leverages iReady [Participation Reports](https://support.clever.com/hc/s/articles/360049642311), more data is available via the [Clever API](https://dev.clever.com/docs/api-overview) feed.

<strong><em>[UPDATE]</strong></em>

| Resource | Description |
| --- | --- |
| [Overview of iReady]() | Intro to iReady, what it can do, and how it can be used. |

## Contributions from the Community

The OEA iReady module [welcomes contributions.](https://github.com/microsoft/OpenEduAnalytics/blob/main/CONTRIBUTING.md) 

This module was developed by the the [Kwantum Analytics](https://www.kwantumedu.com/). The architecture and reference implementation for all modules is built on [Azure Synapse Analytics](https://azure.microsoft.com/en-us/services/synapse-analytics/) - with [Azure Data Lake Storage](https://docs.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-introduction) as the storage backbone, and [Azure Active Directory](https://azure.microsoft.com/en-us/services/active-directory/) providing the role-based access control.

# Legal Notices

Microsoft and any contributors grant you a license to the Microsoft documentation and other content
in this repository under the [Creative Commons Attribution 4.0 International Public License](https://creativecommons.org/licenses/by/4.0/legalcode),
see the [LICENSE](LICENSE) file, and grant you a license to any code in the repository under the [MIT License](https://opensource.org/licenses/MIT), see the
[LICENSE-CODE](LICENSE-CODE) file.

Microsoft, Windows, Microsoft Azure and/or other Microsoft products and services referenced in the documentation
may be either trademarks or registered trademarks of Microsoft in the United States and/or other countries.
The licenses for this project do not grant you rights to use any Microsoft names, logos, or trademarks.
Microsoft's general trademark guidelines can be found at http://go.microsoft.com/fwlink/?LinkID=254653.

Privacy information can be found at https://privacy.microsoft.com/en-us/

Microsoft and any contributors reserve all other rights, whether under their respective copyrights, patents,
or trademarks, whether by implication, estoppel or otherwise.

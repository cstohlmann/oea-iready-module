# Test data

This module includes artifically generated data which matches the format of the four [i-Ready Diagnostic and Personalized Instruction Assessment Reports](https://www.curriculumassociates.com/programs/i-ready-assessment) for both ELA and Math subjects, resulting in a total of eight tables.
- <strong>Comprehensive Student Lesson Activity with Standards Report</strong> provides incremental assessment data on student learning per lesson completed. i-Ready summarizes this data by:
    - the lesson subject area (ELA or Math), 
    - the lesson domain (e.g. phonics, algebra), 
    - additional lesson details (e.g. lesson grade-level), 
    - whether a student passed or failed a particular lesson, 
    - some forms of SIS data (school the student attends, student name, etc.), and
    - lesson correlations with an education system's state standards.
- <strong>Personalized Instruction by Lesson Report</strong> provides the results surrounding student personalized instruction assessments. This table essentially serves as an overview of the <em>Comprehensive Student Lesson Activity with Standards</em> tables, without the matching of state standards.
- <strong>Diagnostic and Instruction YTD Window</strong> provides a year-long snapshot of assessment data on student learning diagnostics. These assessments can be used to identify students who may be at risk for reading/math difficulties. The assessment data also provides test results in specific areas of student-learning domains within ELA and Math. 
- <strong>Diagnostic Results Report</strong> provides the implications and iReady analyses of student diagnostic assessments. These include metrics used for gauging the successes/struggles of student learning (e.g. [Annual Stretch Growth Measure](https://www.curriculumassociates.com/access-and-equity/providing-a-path-to-proficiency-for-every-student)). The assessment data also provides test results in specific areas of student-learning domains within ELA and Math. 

## Data dictionary

### [Comprehensive Student Lesson Activity with Standards ELA Table](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/iReady/test_data/test_data/comprehensive_student_lesson_activity_with_standards_ela/ela.csv)
### [Comprehensive Student Lesson Activity with Standards Math Table](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/iReady/test_data/test_data/comprehensive_student_lesson_activity_with_standards_math/math.csv)

<details><summary>Expand Data Dictionary for: Comprehensive Student Lesson Activity with Standards</summary>
<p>

|Column Name | Data Type | Description |
|-----------|-----------|-----------|
| Last Name | String | The surname of the student. |
| First Name | String | The given name of the student. |
| Student ID | String | The student ID of the student. |
| Student Grade | String | The grade of the student in the education system (e.g. K, 1, 2). |
| Academic Year | String | The academic year of the student at the time of lesson completion. |
| School | String | The name of the school attended by the student. |
| Subject | String | The subject of the lesson (defaulted to "Reading" or "Math" depending on the table). |
| Domain | String | The domain of the lesson; area of learning in the context of the subject area (i.e. Phonics, Comprehension, High-Frequency Words, Phonological Awareness, Vocabulary, Numbers and Operations, Algebra, Measurement and Data, or Geometry). |
| Lesson Grade | String | The iReady-identified grade-level of the lesson. |
| Lesson Level | String | An indicator ("Early", "Mid", "Late", or "Extra") of how the lesson compares to the student, based on the student's grade and the lesson's grade-level <strong><em>[?? UNSURE DUE TO LACK OF DOCUMENTATION]</strong></em>|
| Lesson ID | String | The iReady ID of the associated lesson. |
| Lesson Name | String | The name of lesson. |
| Lesson Objective | String | The learning objective(s) outlined from the lesson. |
| Completion Date | Date | Date the lesson was completed by the student. |
| Total Time on Lesson (min) | Integer | The total number of minutes the student spent on the lesson. |
| Score | Integer | The final score of the student upon completion of the lesson. |
| Passed or Not Passed | String | An indicator ("Passed" or "Not Passed") of whether the student passed the lesson, based on their score exceeds or fails to meet the lesson-score-threshold. |
| Teacher-Assigned Lesson | String | An indicator ("Y" or "N") of whether the student's teacher assigned the lesson to the student. |
| State Standards | String | An abbreviation of the education system's state standards based on their state of residence (e.g. "CA-ELA"). |
| Type of Standard | String | An indicator ("Direct", "Related", "Partial", or "N/A") of whether the lesson belongs or correlates with state standards. |
| Standard Code | String | An abbreviated code for the state standard, to which the the lesson belongs. |
| Standard Text | String | A more in-depth identification of the specific standard, to which the lesson belongs. |

| [CHANGE PICTURE] Comprehensive Student Lesson Activity with Standards Test Data  | 
|:-------------------------:|
| ![](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/test_data_dailypart.png)  |

Notes: 

1) The "Comprehensive Student Lesson Activity with Standards ELA Table" and "Comprehensive Student Lesson Activity with Standards Math Table" have the exact same columns, though the data pertaining to the subject areas differ.

</p>
</details>

### [Personalized Instruction by Lesson ELA Table](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/iReady/test_data/test_data/personalized_instruction_by_lesson_ela/ela.csv)
### [Personalized Instruction by Lesson Math Table](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/iReady/test_data/test_data/personalized_instruction_by_lesson_math/math.csv)

<details><summary>Expand Data Dictionary for: Personalized Instruction by Lesson</summary>
<p>

|Column Name | Data Type | Description |
|-----------|-----------|-----------|
| Last Name | String | The surname of the student. |
| First Name | String | The given name of the student. |
| Student ID | String | The student ID of the student. |
| Student Grade | String | The grade of the student in the education system (e.g. K, 1, 2). |
| Academic Year | String | The academic year of the student at the time of lesson completion. |
| School | String | The name of the school attended by the student. |
| Subject | String | The subject of the lesson (defaulted to "Reading" or "Math" depending on the table). |
| Domain | String | The domain of the lesson; area of learning in the context of the subject area (i.e. Phonics, Comprehension, High-Frequency Words, Phonological Awareness, Vocabulary, Numbers and Operations, Algebra, Measurement and Data, or Geometry). |
| Lesson Grade | String | The iReady-identified grade-level of the lesson. |
| Lesson Level | String | An indicator ("Early", "Mid", "Late", or "Extra") of how the lesson compares to the student, based on the student's grade and the lesson's grade-level <strong><em>[?? UNSURE DUE TO LACK OF DOCUMENTATION]</strong></em>|
| Lesson ID | String | The iReady ID of the associated lesson. |
| Lesson Name | String | The name of lesson. |
| Lesson Objective | String | The learning objective(s) outlined from the lesson. |
| Lesson Language | String | The language in which the lesson was taught. |
| Completion Date | Date | Date the lesson was completed by the student. |
| Total Time on Lesson (min) | Integer | The total number of minutes the student spent on the lesson. |
| Score | Integer | The final score of the student upon completion of the lesson. |
| Passed or Not Passed | String | An indicator ("Passed" or "Not Passed") of whether the student passed the lesson, based on their score exceeds or fails to meet the lesson-score-threshold. |
| Teacher-Assigned Lesson | String | An indicator ("Y" or "N") of whether the student's teacher assigned the lesson to the student. |

| [CHANGE PICTURE] Personalized Instruction by Lesson Test Data  | 
|:-------------------------:|
| ![](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/test_data_resourceusage.png)  |

Notes: 

1) The "Personalized Instruction by Lesson ELA Table" and "Personalized Instruction by Lesson Math Table" have the exact same columns, though the data pertaining to the subject areas differ.

</p>
</details>

### [Diagnostic and Instruction ELA YTD Window Table](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/iReady/test_data/test_data/diagnostic_and_instruction_ela_ytd_window/ela.csv)
### [Diagnostic and Instruction Math YTD Window Table](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/iReady/test_data/test_data/diagnostic_and_instruction_math_ytd_window/math.csv)

<details><summary>Expand Data Dictionary for: Diagnostic and Instruction YTD Window</summary>
<p>

|Column Name | Data Type | Description |
|-----------|-----------|-----------|
| Last Name | String | The surname of the student. |
| First Name | String | The given name of the student. |
| Student ID | String | The student ID of the student. |
| Enrolled | String | An indicator ("Enrolled" or "Not Enrolled") of whether the student is still enrolled at a school. |
| Student Grade | String | The grade of the student in the education system (e.g. K, 1, 2). |
| Academic Year | String | The academic year of the student at the time of lesson completion. |
| School | String | The name of the school attended by the student. |
| Subject | String | The subject of the lesson (defaulted to "Reading" or "Math" depending on the table). |
| User Name | String | The email of the student. |
| Gender | String |	An indicator ("male" or "female") of the student's gender. |
| Hispanic or Latino | String |	An indicator ("Y" or "N") of whether the student is Hispanic or Latino. |
| Race | String | An indicator of the student's racial demographics. |
| English Language Learner | String | An indicator of whether the student is an English language learner. |
| Special Education | String | An indicator of whether the student is in special education. |
| Economically Disadvantaged | String | An indicator of whether the student is economically disadvantaged. |
| Migrant | String | An indicator of whether the student is a migrant. |
| Class(es) | String | An expression for the class(es) that the student is taking. |
| Class Teacher(s) | String | An expression for the teacher(s) that the student has for their class(es). |
| Report Group(s) | String | An expression for the group(s) that the student is associated with at the time of the report generation. |
| Number of Completed Diagnostics during the time frame | Integer | The total number of diagnostic assessments taken at the time of the report generation. |
| Annual Typical Growth Measure | Integer |	An indicator of the yearly expected typical growth. |
| Annual Stretch Growth Measure | Integer |	An indicator of the yearly expected stretch growth. |
| Diagnostic Gain (Note: negative gains=zero) | Integer | An indicator of the general diagnostic assessment growth seen from the student since the latest-previous diagnostic assessment. |
| Diagnostic: Start Date (x) | Date | The start date of the diagnostic assessment. |
| Diagnostic: Completion Date (x) | Date | The completion date of the diagnostic assessment. |
| Diagnostic: Time on Task (min) (x) | Integer | The total time spent on the diagnostic assessment (in minutes). |
| Diagnostic: Rush Flag (x) | String | An indicator of the rush flag association for the student after completion of the diagnostic assessment. |
| Diagnostic: Overall Scale Score (x) | Integer | . |
| Diagnostic: Overall Placement (x) | String | . |
| Diagnostic: Percentile (x) | Integer | . |
| Diagnostic: Overall Relative Placement (x) | String | . |
| Diagnostic: Tier (x) | String | . |
| xxx | xxx | xxx |
| Diagnostic: (_) Measure (x) | String | xxx |
| Diagnostic: (_) Range (x) | String | xxx |
| Diagnostic: Grouping (x) | String | xxx |
| Diagnostic: Language (x) | String | xxx |
| Diagnostic: <strong>(Subject Domain)</strong> Scale Score (x) | Integer | xxx |
| Diagnostic: <strong>(Subject Domain)</strong> Placement (x) | String | xxx |
| Diagnostic: <strong>(Subject Domain)</strong> Relative Placement (x) | String | xxx |
| xxx | xxx | xxx |
| Instruction: <strong>(Subject Domain)</strong> Lessons Passed | Integer | xxx |
| Instruction: <strong>(Subject Domain)</strong> Lessons Not Passed | Integer | xxx |
| Instruction: <strong>(Subject Domain)</strong> Lessons Completed | Integer | xxx |
| Instruction: <strong>(Subject Domain)</strong> Pass Rate (\%) | Integer | xxx |
| Instruction: <strong>(Subject Domain)</strong> Time on Task (min) | Integer | xxx |

| [CHANGE PICTURE] Diagnostic and Instruction YTD Window Test Data  | 
|:-------------------------:|
| ![](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/test_data_resourceusage.png)  |

Notes: 

1) Anything in the above table marked with (x) indicates that the "x" is either replaced with "Most Recent", "1", "2", "3", "4", or "5". 
    - There is a section columns corresponding to each diagnostic assessment indicator.
2) Anything in the above table marked with (\_) indicates that the "\_" is either replaced with "Lexile" or "Quantile" depending on the ELA or Math table, respectively.
3) Anything in the above table marked with <strong>(Subject Domain)</strong> indicates that the entire parenthesis is to be replaced with on of the two sets of domains (the ELA table corresponds with the first set, and the Math table corresponds with the second set):
    - Phonological Awareness, Phonics, High-Frequency Words, Vocabulary, Reading Comprehension: Literature, and Reading Comprehension: Informational Text.
    - Number and Operations, Algebra and Algebraic Thinking, Measurement and Data, and Geometry.
4) With the last "Instruction:" section of columns (outlined above) both tables include an "Overall" section, which precedes the breakdown of subject domains.

</p>
</details>

### [Diagnostic Results ELA Table](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/iReady/test_data/test_data/diagnostic_results_ela/ela.csv)

<details><summary>Expand Data Dictionary for: Diagnostic Results ELA</summary>
<p>

|Column Name | Data Type | Description |
|-----------|-----------|-----------|
| Last Name | String | The surname of the student. |
| First Name | String | The given name of the student. |
| Student ID | String | The student ID of the student. |
| Student Grade | String | The grade of the student in the education system (e.g. K, 1, 2). |
| Academic Year | String | The academic year of the student at the time of lesson completion. |
| School | String | The name of the school attended by the student. |
| Start Date | Date |	Date the diagnostic test was started by the student. |
| Completion Date | Date | Date the diagnostic test was completed by the student. |
| Diagnostic used to establish Growth Measures (Y/N) | String |	An indicator ("Y" or "N") of whether the diagnostic test is used to establish growth measures of the student. |
| Most Recent Diagnostic (Y/N) | String |	<strong><em>[?? UNSURE]</strong></em> |
| Duration (min) | Integer | The total number of minutes the student spent on the diagnostic test. |
| Rush Flag | String |	<strong><em>[?? UNSURE]</strong></em> |
| Overall Scale Score |  |	 |
| Overall Placement |  |	 |
| Overall Relative Placement |  |	 |
| Percentile |  |	 |
| Grouping |  |	 |
| Lexile Measure |  |	 |
| Lexile Range |  |	 |
| Phonological Awareness Scale Score |  |	 |
| Phonological Awareness Placement |  |	 |
| Phonological Awareness Relative Placement |  |	 |
| Phonics Scale Score |  |	 |
| Phonics Placement |  |	 |
| Phonics Relative Placement |  |	 |
| High-Frequency Words Scale Score |  |	 |
| High-Frequency Words Placement |  |	 |
| High-Frequency Words Relative Placement |  |	 |
| Vocabulary Scale Score |  |	 |
| Vocabulary Placement |  |	 |
| Vocabulary Relative Placement |  |	 |
| Reading Comprehension: Literature Scale Score |  |	 |
| Reading Comprehension: Literature Placement |  |	 |
| Reading Comprehension: Literature Relative Placement |  |	 |
| Reading Comprehension: Informational Text Scale Score |  |	 |
| Reading Comprehension: Informational Text Placement |  |	 |
| Reading Comprehension: Informational Text Relative Placement |  |	 |
| Diagnostic Language | |	 |
| Annual Typical Growth Measure |  |	 |
| Annual Stretch Growth Measure |  |	 |
| Mid On Grade Level Scale Score |  |	 |
| Reading Difficulty Indicator (Y/N) |  |	 |

| [CHANGE PICTURE] Diagnostic Results Test Data  | 
|:-------------------------:|
| ![](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/test_data_resourceusage.png)  |

</p>
</details>

### [Diagnostic Results Math Table](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/iReady/test_data/test_data/diagnostic_results_math/math.csv)

<details><summary>Expand Data Dictionary for: Diagnostic Results Math</summary>
<p>

|Column Name | Data Type | Description |
|-----------|-----------|-----------|
| Last Name | String | The surname of the student. |
| First Name | String | The given name of the student. |
| Student ID | String | The student ID of the student. |
| Student Grade | String | The grade of the student in the education system (e.g. K, 1, 2). |
| Academic Year | String | The academic year of the student at the time of lesson completion. |
| School | String | The name of the school attended by the student. |
| Start Date | Date |	Date the diagnostic test was started by the student. |
| Completion Date | Date | Date the diagnostic test was completed by the student. |
| Diagnostic used to establish Growth Measures (Y/N) | String |	An indicator ("Y" or "N") of whether the diagnostic test is used to establish growth measures of the student. |
| Most Recent Diagnostic (Y/N) | String |	<strong><em>[?? UNSURE]</strong></em> |
| Duration (min) | Integer | The total number of minutes the student spent on the diagnostic test. |
| Rush Flag | String |	<strong><em>[?? UNSURE]</strong></em> |
| Overall Scale Score |  |	 |
| Overall Placement |  |	 |
| Overall Relative Placement |  |	 |
| Percentile |  |	 |
| Grouping |  |	 |
| Quantile Measure |  |	 |
| Quantile Range |  |	 |
| Number and Operations Scale Score |  |	 |
| Number and Operations Placement |  |	 |
| Number and Operations Relative Placement |  |	 |
| Algebra and Algebraic Thinking Scale Score |  |	 |
| Algebra and Algebraic Thinking Placement |  |	 |
| Algebra and Algebraic Thinking Relative Placement |  |	 |
| Measurement and Data Scale Score |  |	 |
| Measurement and Data Placement |  |	 |
| Measurement and Data Relative Placement |  |	 |
| Geometry Scale Score |  |	 |
| Geometry Placement |  |	 |
| Geometry Relative Placement |  |	 |
| Diagnostic Language |  |	 |
| Annual Typical Growth Measure |  |	 |
| Annual Stretch Growth Measure |  |	 |
| Mid On Grade Level Scale Score |  |	 |

| [CHANGE PICTURE] Diagnostic Results Test Data  | 
|:-------------------------:|
| ![](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Digital_Learning_Apps_and_Platforms/Clever/docs/images/test_data_resourceusage.png)  |

</p>
</details>

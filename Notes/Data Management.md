From ZIH
Topic : Electronic Lab notebooks 
Technical implementation : Peter Koban 
Torsten Gille 

Translate research work into digital electronic notebook 
raw data into network (backup) processing and into ELN 
ELN is not a data storage - shore information about data 
information about processing of the data 
ELN data share  - and support 
ELN central platform 
What kind of information should go into ELN 
eLABFTW - generic c- experiment and resources 
template for resources and experiment 
connect to store system - not complete raw data 
eLABFTW -SSP 
Time stamp 
ELN archive 
Many people can work on single template 
Web app and API 

Drones managing 
Changelog and scheduler to 
GIt Ci and Cd pipeline eLabFTW pipeline - Git API keys  (line codes) 
Limit 100 MB - 500 MB - Test phase
**Information management platform**  Not data management platform

1. Battery charging and management 
2. communication about what - which data 


Knowledge management 
data, information and knowledge is different 
context to the data is information 
context to information is knowledge 

information - creative act  - knowledge management is art and  difficult act - communicate
eFTW is searchable 

1. kind of data sets 
2. collect , create datasets  identify which kind of datasets
3. cluster , classify based on workflow
4. overview of all experiments

Project management 
research data management 

We have process to take care of the data collection 

Folder based storage structure is one dimensional 
Information management - multi- dimension of storage

Before generating data: 
 resources and processes set and storage system is consistent 
 use eLabFTW to digitalize the process
 

Data architectures and tools and platforms 
Data warehouse enforce in a system
data lake - raw - find pipelines 

Multidimension information for data 
Preflight and post flight 

single dimensional - folder in hierarchical structure 
use a system - network - multi dimensions - entry point of dataset 
eLabFTW as filter  ( not central dependent on hierarchal )
optimise folder structure - also a structure for finding data 
process at eLabFTW 


Our process 
pre-flight experiment 
preparation of flight (organizational) 
drone - actual resources cluster 
external devices 
post-flight 

Consider the datas - how to describe data - data fields 
go pro data 
video, audio - data forat 
location 
who collected data 

flight logs 
position / pose 
location where data is stored 

create resource categories 
template for resources - link to actual resources it create 
template for experiment with drop down menu 
insert details to the fields  - weather , type / information of the flight 
link to produced data 
 generic part - field group - then fields 
export the experiment to any format 

resources go into drone categorize / configuration that can in turn go into experiment 

added / linked into fields are linked down - but into the linked resources don't reflect back to the fields

migration for templates are okay. The data might bot be best due to loss of data - IT protection 

ID for internal 
Own Id - only numbers 

Design decisions 
Pin the templates 
Idea:  Use resource categorizes - hardware version 
"learn to trust the system "

---
8/9 
student tasks managing  stick to git 


---
24/9 elab ftw 
Janna idea 
- User groups 
- students as participants 
- students account details and inform Janna
- Tags in brackets from the first session with Peter and Thorsten
- no capitalization if not the name - visibility 
- permission rights 
- Next meeting 6th october
- what all go in resource description - Gitlab link 
- work on the templates and incident report 

12/1
- Vijaya and Terrence - didn't enter yet 
- feb/march exams 
- Janna Live system 


IT admin
Contact person
how do we use it

---

16/1
 # ELabFTW  communication module template

1. General contact - Storage information 
2. General Device information
	1. Item name  (eg: RC system, telemetry radio )
	2.  Model and Make (holybro, SIYI MK15)
	3. Category/type: It can be a dropdown list with following options - Cellular dongle | Telemetry | Satcom | RC System 
3. Technical Specification 
	1. Frequency bands (eg: 2)
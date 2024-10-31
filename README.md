# Newman_JIRA_Collection_Run

Here, I am creating an Issue in JIRA Site using JIRA RestAPI
--------------------------------------------------------------

===> How we can create an issue manually <===
1.) login to JIRA
2.) Select create button to create an issue
3.) Mandatory field need to be filled to create an issue like
    a) Select Project Name
    b) Select Issue Type (Story, Bug, Task etc.)
    c) Summary for an issue
    d) Select Assignee

===> How We Can Create an Issue using JiRA restAPI <===
Required Credentials
---------------------
1. JIRA API Token (You can generate in the setting)
2. JIRA Resource url (Search JIRA API documentation)
3. JIRA login credential  (Postman Basic Auth)
   a.) username - Your Jira email address
   b.) Password - Your JIRA API Token

A.) Create an Issue through POSTMAN Application
Steps
----
1.) Download JIRA Collection, JIRA Environment and testdata file from github
2.) edit testdata file according to you Jira page
3.) edit environment file and insert you Jira hosturl
4.) Now Import Collection and Environment file in POSTMAN APPLICATION
5.) Go to Run Collection and Select Run Collection Manually
6.) Select inser data files and run the Collection
7.) It will Create the issues in the JIRA

B.) Create an Issue through POSTMAN CLI/ NEWMAN

    1.) POSTMAN CLOUD
       ----------------
    A.) POSTMAN CLI
        ------------
        a) Install Postman CLI
        b) Get Postman API key, Collection Token, Environment Token from Postman Application
        c) Run CMD
        d) Use this command
           postman login --with-api-key {ENTER POSTMAN API KEY with bracket}  ---> login to POSTMAN
           postman collection run {Collection Token without bracket} -e {Environment token without bracket} -d "local data file location"

    2.) POSTMAN CLI without CLOUD
        -------------------------
        a.) Export Collection, Environment file from POSTMAN/ Get Collection,Environment File from github
        b.) Install Postman CLI
        c.) open cmd and run command
        d.) postman collection run "Collection file location address\fileName.json" -e "Environemnt file location address\fileName.json" -d "datafile location\datafile.json or csv"

   3.) Newman 
       ------
        a.) Export Collection, Environment file from POSTMAN/ Get Collection,Environment File from github
        b.) Install Newman
        c.) open cmd and run command
        d.) newman run "Collection file location address\fileName.json" -e "Environemnt file location address\fileName.json" -d "datafile location\datafile.json or csv"
            -r cli,htmlextra  (here -r is use for generating report and you need to install htmlextra using nodjs command)
            --reporter-htmlextra-export "location address (where you want to gnerate the htmlextra report) "

  4.) Jenkin
      -------
     Create a bulid by jenkin configuration with github repo url
     when you run the build it will clone the file from git repo and run collection file with help of Postman CLI/Newman and genrate the report


Note:
-----    NodeJs need to be install and setup in you computer

THANKS,
RISHAB UPADHYAYA
           
   


# CMPG323-Project-2---33296839
API Creation using ASP.NET Core
## API creation
Created the API first on my local machine using the provided documentation. Had minor issues which were resolved quickly. 
### Adding Patch Method
I created a new API (following the documenation) as a new project to add the patch method. After doing research and reading about patch I found the difference between patch and put. Patch Upated a partial record while Put updates the entire record. 
I than updated the original API and added patch by copying the put method and changing put to patch.
#### Adding Authenication to the API
Adding authentication was fairly simple. the issue that were encoumtered was with the migration EF Core commands that were given for creating the package and creating the database and schema. I used the following commands:
To create the migration package used: dotnet ef migrations add InitialCreate
To create the database and schema used: dotnet ef database update
##### Creating Azure database 
This was interesting and simple. The only problem I encountered was with the Firewall settings. AzureDB could not connect to SQL ServerDB. I researched and found that i need to add this rule: start IP: 0.0.0.0	End IP: 255.255.255.255
###### Creation of tables
This was also fairly simple to do. Copied the create table scripts from SQL Server, pasted it in AzureDB and executed the commands.
####### Creating API Managememnt services and Publishing to API from VS to Azure
This was not a problem.
######## Importing the API
Here i had an issue as the site url was not working for me to get the .json swagger path. It kept saying use OpenAPI specified url. I then Publish the package 2 more times until the last one finally worked. Its called ConnectedOfficeFE
######### Issues not resolved 
When trying to post a register Admin in the API, I'm getting an Error 500: Internal server Error. Created APP Service Connection from the Service Connector. Issue is Still persisting.

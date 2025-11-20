# scw-comp

Python project for the weekly competition of [Senior Cubers Worldwide](https://www.facebook.com/groups/1604105099735401).

Reports are published at [https://logiqx.github.io/scw-comp/](https://logiqx.github.io/scw-comp/)


Instructions
------------

Initial Install
 - After cloning the repo and installing Docker and WSL, run the bin/docker_build.sh script to create the Docker components

Processing Results for the current competition:
 - Create a new "YYYY-MM-DD" folder inside the *data/* folder
 - Save the current [Form Responses XLSX](https://logiqx.github.io/scw-comp/responses.html) into this new folder
 - Run the *bin/convert_spreadsheets.sh* sript to pre-process the XLSX
 - If there are any ERRORs generated then fix them in the XLSX manually and rerun the *bin/convert_spreadsheets.sh* script
 - When you are happy the XLSX is correct, run the the *bin/weekly_results.sh* script to update the results pages
 - Take note of the prize winners and enter them into the [Prizes Spreadsheet](https://logiqx.github.io/scw-comp/prizes/winners.html)
 
Generating Scrambles for the new competition:
 - Generate the scrambles using TNoodle and save the resulting zip file to the *scrambles/* folder
 - Unzip the zip file to create a *scrambles/Scrambles for [new date]/* folder
 - Run *bin/weekly_scrambles.sh* to process the TNoodle scrambles and create the competition pages
 - Delete the zip file and its extracted contents
 
Creating new Google Sheet/Form for the new competition:
Sheet:
 - In Google Drive, open the current Responses sheet and choose *File->Make a Copy*
 - In the dialog that appears, change the suggested name to use the new competition start date and remove the "Copy of"
 - Ensure "*Share with the same people*" is selected and then click "*Make a Copy*"
 - After a short while the new sheet will open, delete any existing rows so it is completely empty except for the headings
 - Click the "*Share*" button and copy the link
 - In the repo update both *docs/analytics.html* and *docs/responses.html* to use the new sheet link you just copied
 
Form
 - Back in Google Drive it will have created a new "*Copy of SCW Weekly Comp xxx*" Form when you copied the sheet
 - Rename this new Form to use the new date and remove the "Copy of"
 - Open the Form and change the title to use the new date
 - Click the "*Published*" button and copy the Responder link
 - In the repo update *docs/submit.html* to use the new form link you just copied
 
 
 
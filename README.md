# Automatic-Reminder

UPDATE: To make this script more user-friendly, a Google Add-on Extension for this purpose was created. Using the Google Add-on, one would only need to type in the names and/or only the emails of the participants on the spreadsheet, along with the information related to the event and the structure of the email, and emails would be automatically generated to your participants! The files for this Google Add-on Extension are located within the Add-Ons folder.

Screenshot of the add-on functionality
![](/Google_Addons_Code/add_on_screenshot.png?raw=true "Add-on Example")
------------------------------------------------------------------------------------------------------------------------------------------

This is a Google Script program tailored for Google Spreadsheet so as to automatically generate email reminders (24 hours before the event) to remind participants the time and location of the event, at the same time provide participants with the contact information of the person-in-charge.

The script, AutomaticReminder.gs, was created to tailor for the needs of one of the student clubs I am involved in in college. Anyone who would like to add in this feature to their Google Spreadsheet are welcomed to copy this code and modify it to tailor for their own needs.

To use this script as it is, there are several format requirements for the Google Spreadsheet.
An example of the format is ![](/Spreadsheet_Example.png?raw=true "SpreadSheet Example")

In cell A1, it must be <i>month<i>/<i>day<i> <i>Event Name<i>. Note that after the email is sent, the phrase '(Reminder Sent)' would be added after the event name in cell A1.

For the location in cell A3. it must be <i>'Where: '<i> <i>Event Location<i>, so that the location will be included in the email.
  
For the contact information below for every time slot, it must be <i>time AM/PM/am/pm - time AM/PM/am/pm<i>, then <i>Name<i>, <i>Phone<i>, <i>Email<i>, and anything else after the email column.
  
If there is an officer involved in the timeslot. The row should be either <i>'Officer'<i> or <i>'Officer:'<i>. If there are more than 1 officer during that timeslot, they should be separated with a comma, followed by a white space.

For this script, the script will run automatically everytime a person open the spreadsheet, it will then read it all the sheets in the workbook, then set up to generate email reminders for the nearest time. In this particular example, the program will generate email reminders to Amy and Bob at 9/6 10 AM, a day before the sign-up time. Similarly, Catherine, David and Elaine will receieve their email reminders at 9/6 11 AM.

After the email is being sent at 9/6 10 AM, Bob would received an email like this:

To: dummy1@test.com

Subject: Reminder for Health and Safety Committee Tabling

Hi Bob B,

This is a reminder that you have signed up for the Health and Safety Committee Tabling on 9/7 at 10 AM - 11 AM at MU table #1.

Your officer at that time is Amy A. His/Her contact is (123) 456-7890, dummy@test.com.

From your Officers <3

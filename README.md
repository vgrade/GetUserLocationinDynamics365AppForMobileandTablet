# GetUserLocationinDynamics365AppForPhone
Managed solution compatible with Dynamics 365 v9.x which help you tracking location of crm field user who have access to Dynamics 365 app for mobile and Tablet

Solution Components
1. Userlocation entity which store username, latitude,longitude and full address we get after reverse Geo-coding the latitude and longitude
2. Get address Plugin fetched the full address on the basis latitude and longitude
3. Plugin step which fire on creation of userlocation record
4. Reversegeocoding js web resource - It have js function which retrieve user's location in Dynamics 365 app for Mobile and tablet and store in User Location entity. Also store some additional helper functions.

To Do:-
1. Download the solution, unzip it and get the crm solution zipped file (TrackUserLocationinDynamics365App_tobeImportedintoCRM) from it and import into your crm instance
2. On the event on which you want to check in location, call the function getcurrentLocation from Reversegeocoding js library.(In this solution i have called it on check-in and check-out field on appintment entity) 
3. Enable location in your  Dynamics 365 app for Mobile and tablet
4. Make sure plugin step is enabled
5. Upload the UserLocationtobeUploaded available in solution into your crm organisation and check userlocation entity records got created (Optional step)
6. Open a user record, you'll see map in Track User tab and Location history tab to show location history
7. New feature: added from Date and To Date field on system user form. User can specify the date range and click track to track the location of specific time period. By default system show last 20 locations of the user.

For help,please contact grade.vishal@gmail.com

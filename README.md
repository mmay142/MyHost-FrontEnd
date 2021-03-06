# MyHost-FrontEnd
Front End code for MyHost application project

30 Oct 2021
Started login screen. The webpage still looks good when resized and appears to be compatible with mobile.

01-02 Nov 2021
Added User home screen, basic table layout, and jquery functionality
Added tableTemplate.html for table selection, passing selected table to tableTemplate functionality, converted jquery back to javascript functionality

03 Nov 2021 (at 1 am...)
Added functionality to tableTemplate.html using sessionStorage to pass table selection information to change template to selected table. So far, only the table displayed, table name,
and how many seats the selection has changed. Need to create a dyanmic change for the placeholder time and adjust table sizing. Plan to code confirm table selection next.

Added nav bar that we can add more buttons if necessarily and css to go along. No functionality for the logout or account buttons yet.
Added pop up tests for table reservation page.

07 Nov 2021
1. Added CSS grid to Table Template file to make customization easier. Also added a form for entering information for table and separate stylesheet for table template.
2. Added login styles css file / updated login input css
3. Added sign up styles css file / updated sign up input css
4. Adjusted table template so max attribute of input for partySize to match max seats for table type selected
5. Added error handling on booking details for phone number, and option to opt in or out of automatic table swapping
6. Updated table template size display from scale(1) --> scale(1.5)

08 Nov 2021
1. Added admin view home page and some basic information. Added buttons to navigation bar to switch between admin view and user view for placeholder purposes.
2. Updated links for buttons on navigation bar to inherit color so text isn't blue anymore + MyHost now is a button to home page.
3. Added admin view table layout page, adjusted some formatting. Will plan to add customizable...grid. Work in progress and patience.

12 Nov 2021
1. Adding adminLayout html and style sheet for html page. Adding an incomplete layout html and plan to add more. Wanted to go ahead and add to project.

19 Nov 2021
1. Pushing updated CSS table layout for admin view. No functionality yet. Plan to work on client/host requests.

30 Nov 2021
Sorry for lateness ;n; updated tableMap.html to have provided string parsing functions when sockets implemented. Two functions for either each string or one entire string.

01 Dec 2021
Added functions for string parsing on tableTemplate.html to parse replies from the server. Functions will take replies that the client requests (how many groups in queue) and display
a wait time and number of groups ahead of you in queue for a specific table

05 Dec 2021: Added function for creating request string for group reservation.

06 Dec 2021: 
1. Added async function for sending server request for table availability and parsing reply to update table map.
2. Added refresh button for refreshing queue for each table. Could not get onload to work without waiting for the
socket to finish. 
3. Added reservation creation code for creating group that will be added to queue with necessary information.

07-08 Dec 2021:
1. Added background image to tableTemplate and formatted background for Active Reservations
2. Created session storage item on tableTemplate to send to User Home Page to display
3. Create code to parse information set by session storage item to display to user (their current reservation)
4. Set up test polling function on user home page to check for reservation updates.
5. Added cancel button for reservation
6. Adjusted validation for user entering number higher than max seats for table
7. Restaurant name changes depending on what button is pressed
8. Updated UserHomePage to send request to backend to update queue wait time and display reply
9. Updated UserHomePage for function to be called when cancelling, just need backend code, also updated Admin View --> Admin View (Beta)
10. Added polling function to table map to update every 5 seconds

09 Dec 2021:
1. Final touches. Implemented cancel function. Will either cancel reservation if in queue or tell customer to contact restaurant if ready
2. Added comments to tableTemplate and tableMap htmls
3. Session is cleared when logging out for prototype purposes

-----------------------------------------------
# Completed Steps:
1. Organize and develop created home screen
2. Figure out how to make interactive pages for the table configurations / choose table in restaurant
3. Create booking screen for restaurant
4. Created test functions for socket string parsing for some of the html pages
5. Work on functions in tableTemplate.html for confirming group reservation to send to server.
6. Clean up User Home Screen, fix font discrepancy 

# Next Steps:
<<<<<<< HEAD
1. Work out client-server requests for smooth transition of connecting backend to frontend: **Completed, finishing testing**
2. Adjust background images for pages **In Progress**
3. Format current reservation with queue time on UserHomePage **InProgress**

#On Hold Steps:
1. Create web notification that a different table is available: **Canceled --> Automatically change table is opt in**
2. Create admin view for managing tables: **On hold**
3. create admin view for moving tables in or out of the restaurant: **On hold**

# Later Steps:
[ ] 1. Add javascript for login and registration in the login.html and signup.html pages. 
[ ] 2. Connect the front end to the backend via sockets. JavaScript -> Java



# Notes for Website <---> Server (backend) communication
1. Do we use sockets for communication? 
   This would involve the frequent communication of persistent sockets.

2. Create temporary sockets sending json objects back and forth for details? 







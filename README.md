# GardeningWizard

Code: https://drive.google.com/file/d/1NjJwHcC7b0Eh4E68-UDAy_7mQFjxwUVV/view?usp=share_link 

Requirements specifications

●	Plant Library: Plant Library contains the prototype of the real-time data. It includes a comprehensive list of plants that can be grown indoors. Basic information like common name, scientific name and image is added about each plant.

●	Add to list: There is an option to add to list next to each plant entry to the wishlist of the user. Once the plant is added to the wishlist, the button changes to an unclickable state to avoid duplicate entries.

●	Plant profile: On clicking each plant in the list, the complete profile of the plant is loaded. It contains information about soil mixture, water needs, best time to sow and harvest.

●	User profile: User profile contains user name, brief bio, and wish list. Reminder icon at the top right corner allows the user to set reminders to water their plants.

●	Q&A forum: Q&A sections allow the user to interact with other gardeners. It is organized as two tabs: one for posting their questions and another for answering the queries asked by others.

●	Menu bar: There is a menu bar at the bottom of the app to easily navigate between the home page, user profile and Q&A section.


Technical description

Home Section:

The Home section is a crucial part of the application’s home section, which is implemented in the files activity_main.xml and MainActivity.java, It provides access to a wide range of plant options that can be added to the user's wishlist. When the user clicks on the plant name, the corresponding activity for the plant starts displaying detailed information about the plant. The methods addCorn, addRadish, addBeans, addCarrot, and addCabbage handle the user’s action of adding a plant to the list. When the user clicks on the add to list button, the corresponding method is triggered, the plant which is selected is added to plant ArrayList, and the text on the button gets updated to “Added” and it is set unclickable which indicates that the plant has been added. This feature eliminates the duplicate entries being added to the list.

<img width="215" alt="Screenshot 2023-09-11 at 3 38 27 PM" src="https://github.com/laasya2005/GardeningWizard/assets/71040750/f98cba6e-953c-4518-90af-ddd009d4cb36">

Profile Section:

The files activity_profile.xml and profileActivity.java, are responsible for managing the user’s profile within the application. It consists of three sections - bio, wishlist, reminder. The plants added to the list from the home screen through intent extras are populated in the wishlist. User information like name and bio are added as editable text. It also has a feature to set reminders to water the plants.   The method onClickRemainder() is triggered when the user clicks on the reminder button. It opens the default calendar application on the mobile and populates a few fields.

<img width="654" alt="Screenshot 2023-09-11 at 3 33 33 PM" src="https://github.com/laasya2005/GardeningWizard/assets/71040750/ed28d85c-f2bc-4c4e-a261-1a96f8b145dd">

Plant Profiles:

The plant profiles give all the major information required to grow a plant. The functionality is implemented in corresponding activity files for example CabbageProfileActivity. Images of the plant and other information are loaded from the source folder.

<img width="799" alt="Screenshot 2023-09-11 at 3 34 49 PM" src="https://github.com/laasya2005/GardeningWizard/assets/71040750/aa8460ec-2488-40ad-8994-8648f2f33d99">

Q&A Section:

This section includes QuestionAnswerActivity.java manages interaction between the tabs and DBHandler class. The methods onQuestionPosted() and onSaveAnswer() are used to add questions posted and answers recorded to the database. It has OnTabSelectedListener to monitor the tab activities, to check if the tab is selected or unselected.

AskQuestionFragment is the corresponding activity to ask a question tab. When the user posts their question, the content from the edit text is passed to QuestionAnswerActivity and it in turn is added to the database. Once the question is posted, a toast message is displayed to show that the response is recorded.

ViewQuestionsFragment is the corresponding activity for viewing the questions posted by everyone. The latest two questions and their answers are displayed. There is an edit text view to answer the questions posted. Once it is posted, the OnSaveAnswer() method from QuestionAnswerActivity is called and the page is refreshed with new contents.

<img width="485" alt="Screenshot 2023-09-11 at 3 35 35 PM" src="https://github.com/laasya2005/GardeningWizard/assets/71040750/40bc0909-a6f9-4e9e-929e-5f3de845906f">


SQLite Database:

Q&A forum is implemented using SQLite Database. It has two modal classes QnAModal and AnswerModal for two tables. We have DBHandler classes with methods to add to the tables and methods to read the data from the table. 

Menu Bar:

Menu bar has OnMenuItemClickListener to handle the clicks in the menu bar. It gets the id of the item clicked using item.getItemId() and based on the id, the activity is called. If id is R.id.menu_home, home is populated and if id is R.id.menu_profile, profile activity is populated, similarly if id is R.id.menu_qna, QnA activity is loaded.


Future Enhancements:

Gardening Wizard is a growing application with the scope for future enhancements. Some future improvements include:

●	Introducing the gardening tips area, with insightful advice from professionals

●	Adding more interactive features to the Q&A community like upvoting.

●	Including video-based plant care tutorials 

●	Making use of API to provide real-time plant library

Brief Instructions for using the app: 

1.	Start: Click on the application to launch the Gardening wizard app.
   
2.	Plant Library: You can scroll through the comprehensive list of domestic plants. You can also add plants to your collection(wishlist) using the “Add To List” button.
   
3.	Plant Profile: To view detailed information about the plant, click on its name on the homescreen.
   
4.	User Profile: If you wish to edit your name and bio, you can edit them here. You can also view the plants wishlisted.
   
5.	Watering Reminder: You can click the bell icon on the top right corner of the profile section. This allows you to set reminders through the default calendar.
    
6.	Q&A Section: If you want to post a question then you can click on ask a question tab. If you wish to answer previously asked questions, you can enter the answer in the appropriate box and click on answer.

Conclusion:

Thus Gardening Wizard offers a dynamic platform to explore, learn, and connect with enthusiasts around the world. It is the ideal gardening partner because of its comprehensive plant collection, in-depth plant profiles, vibrant Q&A platform, and customized user profiles. The app has a colorful and user-friendly UI making gardening an enjoyable and rewarding experience for people everywhere. By integrating real-time data, our application will have the potential to revolutionize the gardening software market.


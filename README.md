
<h1 align="center">Radiology Outpatient Order Board App</h1>
<h1 align="center"><img src="https://github.com/BrianLipscombe/radiology-outpatient-board/blob/main/static/images/banner.jpg?raw=true" /></h1>

This is Brian Lipscombe's third Milestone Project at [Code Institute](https://codeinstitute.net). It was built using HTML5, CSS3, JavaScript, Python+Flask, MongoDB, Gitpod, and deployed on the hosting platform Heroku. It is designed with Code Institute's Assessment Handbook Project Idea 0 in mind - Bring your own idea to life, based on providing value to users to address a specific real or imagined need.

It is not intended for public use but instead intended to provide management support for orders within a radiology department, or tandem group of radiology departments, within a hospital setting. In such a busy setting, balancing scheduled appointments for outpatients with spontaneous STAT orders being placed from the Emergency Department as well as prolonged, complicated exam orders from the Intensive Care Unit can be very challenging, and an app like this could provide some added organization and time-management.  

The app can be found on Heroku [here.](https://8080-brianlipscombe-radiology-2sjdmmrwjw4.ws-us31.gitpod.io/get_tasks)

## User Experience (UX)

* User Stories

1. Radiology Employee Goals
    - Register a username and password
    - Log in
    - Add outpatient orders from hardcopies in fax basket, including modality, patient name, exam description, date, time, any pertinent comments, and indicate whether the exam is urgent or not
    - Edit orders if any information changes
    - Delete completed orders

2. Owner Goals   
    - Allow radiology employees to input, edit, complete, and manage outpatient orders more effeciently.
    - Ensure only registered staff memnbers have access to the app and is only used within the radiology department to protect patient information.
    - Allow users to create new profiles. 

* Design

1. Color Scheme

    - Black is used for each collapsible header because in some hospitals radiology teams wear black scrubs to quickly differentiate from other hospital staff members.
    - White with a bit transparency is used to add contrast against the black headers.
    - Red is used in the top navbar to mimic the hospital's red exterior signage.
    - Blues are used in some text and buttons to contrast the urgency of red, to bring a form of aesthetic balance.  

2. Imagery

    The background image was taken from the UCI Medical Center website [here](https://uci.edu/presidential-gateway/overview/_img/overview-future-hospital-1200x570.jpg) then modified using Adobe Photoshop.

3. Typography

    The fonts are kept basic for easy readability.

* Wireframe

    View the Balsamiq wireframe [here.](https://slack-files.com/T0L30B202-F032TL0U7FZ-9c9a17a249)

## Features

* Responsive on all device sizes.
* Interactive elements: Search bar, Buttons, collapsible popout, and calendar date picker. 
* Ability to create, read, upadate, and delete orders.

## Technologies Used

* [HTML5](https://en.wikipedia.org/wiki/HTML5)

* [CSS3](https://en.wikipedia.org/wiki/CSS)

* [JavaScript](https://en.wikipedia.org/wiki/JavaScript)

* [Python3](https://www.python.org/download/releases/3.0/)

* [MongoDB](https://www.mongodb.com/)

* [Heroku](https://signup.heroku.com/)

* [Font Awesome](https://fontawesome.com/)

* [Github](https://github.com/)

* [Gitpod](https://www.gitpod.io/)

* [Git](https://en.wikipedia.org/wiki/Git)

* [Chrome Dev Tools](https://developer.chrome.com/docs/devtools/)

* [Balsamiq](https://balsamiq.com/)

## Testing

1. Manual Testing
* Buttons
    - If register button is clicked, register page allows user to register username and password.
    - If Log In button is clicked, log in page allows user to input username and password to access the order board.
    - If All Orders button is clicked, user is brought back to the main page.


* Collapsible
    - If the arrow buttons are clicked, the popup opens displaying the modality, exam description, patient's name, and the username of the tech who added the order.
    - If the user is logged in and if the complete/delete button is clicked, the order is removed from the database.
    - If the user is logged in and the edit button is clicked, the edit task page aloows the user to edit the order.
    
* Responsiveness

    - This project is confirmed to be responsive on all standard screen sizes using the devtools device toolbar

* Browser Validation

    - This project is confirmed to work with different browsers: Chrome and Internet Explorer

2. Automated Testing

* Code Testing 

    - This project has been tested using different browsers and different mobile devices such as iphone, Android, and laptops, as well as on a desktop computer.

    * Lighthouse Auditing

        - This project scores 100 for Accessibility and Best Practices for mobile devices, and 100 for Accessibility, Best Practices, and Performance for desktop devices

All pages were tested on multiple resolutions for proper responsiveness.

All files and pages were validated by direct input with no syntax errors using:

* [Nu Html Checker](https://validator.w3.org/#validate_by_input)
* [W3C CSS Validation Service](https://jigsaw.w3.org/css-validator/)
* [JSHint](https://jshint.com/)

<a name="deployment"></a>
## Deployment

- ### Local copy
1. Install all the requirements: Go to the workspace. In the terminal window type: pip3 install -r requirements.txt.
2. Create a database in MongoDB
    - Signup and login to MongoDB account.
    - Create a cluster and a database.
    - Create a collection in the db: categories, tasks, and users.
    - Add string values for the collection.
3. Create the environment variables
    - Create a .gitignore file in the root directory of the project.
    - Add the env.py file in the .gitignore.
    - Create the file env.py. This will contain all the envornment variables.
    - Import os
    - os.environ.setdefault("IP", "Added by developer")
    - os.environ.setdefault("PORT", "Added by developer")
    - os.environ.setdefault("SECRET_KEY", "Added by developer")
    - os.environ.setdefault("MONGO_URI", "Added by developer")
    - os.environ.setdefault("MONGO_DBNAME", "Added by developer")
  4. Run the app: Type python3 app.py in the terminal.
  
- ### Heroku Deployment
1. Set up local workspace for Heroku
    - In terminal window type: pip3 freeze -- local > requirements.txt. (The file is needed for Heroku to know which filed to install.)
    - In termial window type: python app.py > Procfile (The file is needed for Heroku to know which file is needed as entry point.)
2. Set up Heroku: create a Heroku account and create a new app and select region.
3. Deployment method 'Github'
    - Click on the Connect to GitHub section in the deploy tab in Heroku.
    - Search to connect with the proper repository.
    - When repository appears click on connect to connect the repository with Heroku.
    - Go to the settings app in Heroku and go to Config Vars. Click on Reveal Config Vars.
    - Enter the variables contained in your env.py file. it is about: IP, PORT, SECRET_KEY, MONGO_URI, MONGO_DBNAME
4. Push the requirements.txt and Procfile to repository.
    - $ git add requirements.txt
    - $ git commit -m "Add requirements.txt"
    - $ git add Procfile 
    - $ git commit -m "Add Procfile"
5. Automatic deployment: Go to the deploy tab in Heroku and scroll down to Aotmatic deployments. Click on Enable Automatic Deploys. By Manual deploy click on Deploy Branch.

  Heroku will receive the code from Github and host the app using the required packages. Click on Open app in the right corner of Heroku account. The app wil open and the live link is available from the address bar.

## Known Bugs

* Sometimes the exam date and appointment time options will not function properly when clicked on. Other times they do function properly, especially if the tab button is used to advance into those input fields instead of clicking directly on them.
* Editing orders will lead to error page (this error has been fixed by updating the requirements.txt file).

## Future Improvements

* Add better CRUD functionality for users to edit their profiles.
* Make entities more consistent. Instead of using tasks and orders for the same purpose, make all entities into orders, not tasks.
* Make the collapsible display orders in chronological order by the importance of the due dates, instead of by the order of when new orders were added.
* Improve the visibilty of the lower page text such as on the Log In and Regester pages.

## Credits

* Code

    Code used as a template was borrowed from the Code Institute Data Centric Design Mini Project by Tim Nelson [here](https://learn.codeinstitute.net/courses/course-v1:CodeInstitute+DCP101+2017_T3/courseware/9e2f12f5584e48acb3c29e9b0d7cc4fe/054c3813e82e4195b5a4d8cd8a99ebaa/) with his final Github commit [here.](https://github.com/Code-Institute-Solutions/TaskManagerAuth/tree/main/08-SearchingWithinTheDatabase/01-text_index_searching)
    
    Code for icons from [Font Awesome](https://fontawesome.com/).

    All other code was written by the developer.

## Acknowledgements

* Guidance and Moral Support

    Caleb Mbakwe: My mentor Caleb for helping me and for providing professional feedback even though time and scheduling has been an enormous challenge for me;

    Code Institute on Slack;

    And, my family for being patient and understanding when most of my time is absorbed by work and school. 

This site was developed for educational purposes.
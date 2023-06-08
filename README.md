Course Waitlists
=============
### Authors: Calvin Eng, Aanya Hudda, Tabitha Lynn, Shravya Sompalli
Link to Project-
https://github.com/Calvineng72/Course-Waitlists
## Project Details
Course Waitlists is a project dedicated to solving issues related to course registration, focusing specifically on course waitlists. In order to reduce stress, our web application allows students to join and leave course waitlists if they are unable to register for a class. Students can view their position relative to other students, and as an additional feature, have the option to receive course recommendations. Our algorithm suggests courses based on the waitlists of other students interested in the same class. 
## Design Choices

FRONTEND
On the frontend, we decided to implement Next.js as the main framework for our app. Next.js provided us with in-depth tutorials and examples for the frontend design that we were hoping to achieve. We also wanted to learn how to use Next.js as a learning experience; it was really interesting to implement a framework that we haven't used before and learn what it's like to utilize online resources to teach ourselves. 

We decided to implement Google Authentication into a sign in button instead of making it a first page that prevents you from entering the screen before you sign in. There was a couple of reasons for this choice, but one of them was simply being able to see the page whether or not you've logged in now. In retrospect, we did not fully consider the security of this choice; anyone, regardless of if they go to Brown or not, can see the every class and the waitlists. However, if we wanted to be able to put up the website and link it in our resumes, having a site available to everyone would be beneficial. 

We also chose to use Next Auth instead of Google OAuth. Although we attempted both, Next Auth provided the best built-in structure user authentication. This method of authentication also makes it verys simple to add in another authentication provider (i.e. Github). 

For our front-end styles, we prioritized accessibility for users. The font we used, Verdana, is listed as one of the most accessible CSS font families. Additionally, we played close attention to the contrast of the colors to provide the most accessible user experience. That included a higher font-weight for the header, a non-white color when the class boxes are hovered over, white text against a blue background in each class, and a clear red X for removing yourself from the waitlist.  


BACKEND
In terms of the background, the biggest decision we made was to keep the waitlists in a SQL database. We considered other methods that were common for the final project, like Mongo and Firebase, but we ultiamtely decided that SQL would be the simplest way to accomplish our goals. SQL is a simple way of storing data — especially because our courselist/student data was on the more simplistic end — and we knew it was compatible with Java. After speaking to a TA in collab hours, and discussing more in depth with our mentor TA, we also came to the conclusion that the 32 TAs all had at least some experience with SQL (because of the lab last year) and would be able to support us to some capacity. 

One of first choices we had to make as we were narrowing the scope of our project was who our target user was. Originally we thought about having two different user profiles have different capabilties, but we decided that we wanted our main focus to be on the students. As students ourselves, we know firsthand the direct desires of students from a waitlsit app, so being able to implement the user experience for students would be much easier. Based on our cumulative knowledge and goals for the project, we decided to narrow the focus of the app to be student-facing. This meant that our backend database was hardcoded by us, with the understanding that if used in a real scenario, that would the equivalent of a professor being able to change people on the list at will.

## ERRORS AND BUGS
- Button has to be pressed twice to remove someone or join the queue    

## TESTING
Backend
- Unit testing
- Integration testing (mocked)

#### HOW TO
To use our app, a developer must first start the server in the backend. To do so, open the term project in IntelliJ through the pom.xml. Then start the server by pressing the play button in the server class. The backend is now running and fetch calls from the frontend will be successful. To start the frontend, open the entire term project in VS code. Then type "npm run dev" into the terminal. Once it runs, the link "localhost:3000" will open the Waitlist App home page containing each class. The sign-in button on the top right of the header will allow access to joining the waitlists once signed in through a Brown email. A user can click on their desired class to see the current waitlist, and add themselves using the "Join Queue" button. If the user is already on the waitlist, clicking the red X will remove them the waitlist. 

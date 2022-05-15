<h1>Week 1</h1>

<h3>Thursday March 31</h3> We had a meeting where we discusses who were interested in what parts of the project, general ideas regarding the requirements and some ideas on how to tackle them.

As we are 4 members from the DIS program we decided that they will be working on the robot and the rest of us will be split into a mobile-backend team. The mobile-backend team is meant to be flexible, so that we can swap around people if some technical part require more man power. This works because we share very similar backgrounds between the exchange students and the DMP students.

Each team started working on some preparatory work for the next week. I took part in discussing the database structure and we also discussed how the mower shall connect the backend in terms of steering from the app. Right now it seems the app will be sending a signal to either go forward, backwards, left, right or stop. It will be a continous stream of this 1 state.

We will be adopting the SCRUM methodology for our work.



<h1>Week 2 - 20h</h1>

<h3> Monday 4 April</h3>  We did estimations and started working on our parts that we were assigned. I will be working with Killian on the mobile app this week. After the sprint planning it was time for other studies, and not much more was done today.

<h3>Tuesday 5 April</h3>

Today we had a short sprint planning but I could not show very much because I started working on the app today. I setup the ground work for a lot of the app, including making sure the packages Retrofit2, GSON and OkHttp works. They are used to send http requests via Android native. I also tested the stuff with a mock API and it works so I feel its a job well done.

<h3>Wednesday 6 April</h3>

As I finished most of my tasks yesterday, I was mostly helping my teammate,  he has worked with Android and Kotlin before but was sometime ago so he needed some refreshment some topics. It was going fine but unfortunately there was a lot of version errors with dependencies and also with Android Studio. We did fix in the end, but a lot of time was spent debugging and looking into different versions of packages. A rough day productivity wise, but progress was made nonetheless.

<h3>Thursday 7 April</h3>

Today we had our first retrospective. Everyone agreed that in general it was a really good week. The robot team showed some nice progress with mower and how it can detect black lines before it. We from the mobile did not show anything visual because there is barely anything visual that has been done, but we informed the rest that we can contact APIs correctly, so as soon as the real API is up we can connect. The backend team has finished the backend skeleton and is ready to set it up to AWS so next week some real progress will probably be made.

One problem we had faced was that many of us believe that our schedule is a bit messed up. We changed time of meetings several times because it is very hard to make sure everyone can attend everytime. But the times we have decided on now should be fine for everybody so going forward it should be better.

<h1>Week 3 - 25h</h1>

<h3>Monday 11 April</h3>

Online sprint planning with everyone. I am going to continue working with the app and we intend to finish all the setup this week. As we resolved the dependencies last week we should be able to implement it rather quickly. 1 More teammate will join the app work this week, he will focus mostly on UX meanwhile I will finish the setup stuff that was behind. The plan is finish the setup tomorrow (because I dont have time work on this project on mondays) and then start doing the views and finish them before the end of the week.

<h3>Tuesday 12 April</h3>

So we decided that I will not be doing the setup, rather I will just be reading documentation and working on some minor UX stuff.

<h3>Wednesday 13 April</h3>

Still reading documentation to understand how to correctly use MVVM structure for the project. Killian is working on implementation and is soon getting it done. I try to help whenever he needs help.

<h3>Thursday 14 April</h3>

MVVM structure is finished. Good job Killian. The retrospective was on discord because the lecture was on Zoom.  There were 1 person reported missing from the Mower-team. It was reported that we need a day where we decide upon some interface structure for the communication between mower-cloud-app.

<h1>Week 4 - 22h</h1>

<h3>Tuesday 19</h3>

Monday was a red day so no sprint planning then. It was today instead and we decided to work on getting the connection complete this week. The app is ready to send http requests to the backend and the backend will be put up on a server this week. The mower will focus on it as well. Bluetooth will be the next step for next week.

<h3>Wednesday 20</h3>

Today I worked on merging the views to our new MVVM structure. The views was done in another branch on the side, so today when we were going to marge it was a bit of changes that needed to be done for conflicts. I worked on this with Killian and Ivin. After that we set it up so that we cleaned up a lot of code and are not using unnecessary code. It was a good day, we are ready for demo tomorrow where we will show the app and the views working correctly and being able to connect to API.

<h3>Thursday 21 April</h3>

Today I demo'ed the App for the rest of the team and showed our http request to a mock api as well as our views and how it will look. The views that are not finished are the map view and controller. The map we are waiting a bit with because we dont know how to handle the drawing of the position of the mower yet.

<h1> Week 5 - 13h</h1>

<h3>Monday  25 April</h3>

I did not work today on the project but I went to the lecture. I attended the sprint plan and we decided to finish the connection between the different parts and to send a hello-world from app -> cloud -> mower.  It will be tested on thursday on our demo. Some views need to be correctly integrated, we are missing for example the controller (its 90% finished) and the map. Will need to talk to Ivin and Killian to sort this.

<h3>Tuesday 26 April</h3>

I attended the standup, but had to work on other courses. The api went up today, so I did some testing towards it Postman and it worked great.

<h3>Wednesday 27 April</h3>

I attended the standup today as well, but I still had to work on other courses today. Will catchup on Friday / the weekend.

<h3>Thursday 28 April</h3>

I attended the demo, catched up with Killian and Ivin and the views are looking good. I can easily integrate them into the app next week. I can also be way more efficient in this course because there will be less pressure from the thesis work. The demo went well, we got to see the mower in partial action and it does look nice.

<h3>Sunday 1 May</h3>

Looked into the requirements for the project as a whole. We have a whole lot of documentation to write, which I started today. I also noticed we need to do a Lesson Learned Document which I will inform the team about tomorrow. I started on the documentation, and looked for potential things we may have missed in the problem requirements.

<h1>Week 6 - 20h</h1>

<h3>Monday 2 May</h3>

Sprint planning at 9, I mentioned the documentation writing that all teams needs to do. Also about the lesson learned document. As I looked more into the requirements yesterday I think I understood what we need to do moving forward better and explained some of this to the team. 

We were discussing how to visualize the path. Didde mentioned that the XY coordinates will be in a continuous stream and in a very long DB table. This will clutter the path the longer you have the mower going. I suggested splitting it into different runtime sections. So after each "pause" or "sleep" command, the next session will be counted as a completely new drive. The clutter on the visualization will be less, and the structure of the system will be more scalable I believe. 

I today merged together the UI branch and the API branch. The only view left is visualize_path which I am going to work on the remainder of the week on. There was a lot of conflict for the merge so it took a long time. I also changed so we can send api requests to the actual API and use the information we get, so for example we display the mower name on the first page now directly from API. Worked together with Killian on this. Tomorrow I will look into visualizing the path.

<h3>Tuesday 3 May</h3>

Looked into the drawing of path visualization. I attempted to create a canvas and draw on it, but it conflicted with our dependency injection. Not sure how to proceed from here, need to talk to Killian.

<h3>Wednesday 4 May</h3>

More of yesterday, debugging what could be wrong and cause the issue. It seems, as we need to extend a fragment with the View class, but I cannot do that because we use dependency injection. Next week I will need to sort this out preferably with Killian as he is the go-to-guy for MVVM stuff now.

<h3>Thursday 5 May</h3>

For the demo I was there but had no real progress to show, but it was still nice to see where everyone is at and all. We discussed a lot of potential documents we need to write before we finish the project, like the WBS and project description. Luckily I have already done a bit of project description so that should be fine. We agreed that someone should talk to Andreas about what counts as a WBS, but as I am writing this I think we did not assign anyone to this, so it will probably be forgotten until I read this ...

<h1> Week 7 - 23h</h1>

<h3>Monday 9 May</h3>

Attended the sprint planning at 9.  We agreed upon a session where all teams gather and you code together and or test stuff. It will probably be wednesday if all goes according to plan. I am still tasked with doing the path visualization as well the API requests to start autonomous driving. The api request I can fix but path visualization is harder than I imagined. On wednesday I will be able to work fulltime on this project as I should finish my thesis work for tomorrow.

<h3>Tuesday 12 May</h3>

Fixed starting and stopping for autonomous driving. Works great with app -> postman, so it should work well with the actual mower too. Will have to test it on thursday. Told Yev that we need more clarifications on what the WBS and project description and lesson learned document is. He should bring this up on his thursday meeting with Husqvarna.

<h3>Wednesday 11 May</h3>

Looked more into path visualization, found a potential way of making it work via using creating a class that extends Drawable(), but will have to test later, too tired after looking into the best possiblities for this...

<h3>Thursday 12 May</h3>

Demo. We watched the mover doing it testing and it seemed good. The app is ready with starting and stopping autonomous driving. Unfortunately the mower team did not have the proper setup for us test the start-stop autonomous driving. After the demo Yev and I sat with trying to get the permissions to work for bluetooth. We did not solve it on the spot, but when I got home I started googling and found a potential fix, he said he was going to try and implement it, will hear from him on Monday.

<h3>Sunday 15 May</h3>

Got drawLine to work with the Drawable class. Started setting up so we can fetch the datapoints.


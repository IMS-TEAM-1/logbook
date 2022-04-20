<h1>Week 1</h1>

<h3>Thursday March 31</h3> We had a meeting where we discusses who were interested in what parts of the project, general ideas regarding the requirements and some ideas on how to tackle them.

As we are 4 members from the DIS program we decided that they will be working on the robot and the rest of us will be split into a mobile-backend team. The mobile-backend team is meant to be flexible, so that we can swap around people if some technical part require more man power. This works because we share very similar backgrounds between the exchange students and the DMP students.

Each team started working on some preparatory work for the next week. I took part in discussing the database structure and we also discussed how the mower shall connect the backend in terms of steering from the app. Right now it seems the app will be sending a signal to either go forward, backwards, left, right or stop. It will be a continous stream of this 1 state.

We will be adopting the SCRUM methodology for our work.



<h1>Week 2</h1>

<h3> Monday 4 April</h3>  We did estimations and started working on our parts that we were assigned. I will be working with Killian on the mobile app this week. After the sprint planning it was time for other studies, and not much more was done today.

<h3>Tuesday 5 April</h3>

Today we had a short sprint planning but I could not show very much because I started working on the app today. I setup the ground work for a lot of the app, including making sure the packages Retrofit2, GSON and OkHttp works. They are used to send http requests via Android native. I also tested the stuff with a mock API and it works so I feel its a job well done.

<h3>Wednesday 6 April</h3>

As I finished most of my tasks yesterday, I was mostly helping my teammate,  he has worked with Android and Kotlin before but was sometime ago so he needed some refreshment some topics. It was going fine but unfortunately there was a lot of version errors with dependencies and also with Android Studio. We did fix in the end, but a lot of time was spent debugging and looking into different versions of packages. A rough day productivity wise, but progress was made nonetheless.

<h3>Thursday 7 April</h3>

Today we had our first retrospective. Everyone agreed that in general it was a really good week. The robot team showed some nice progress with mower and how it can detect black lines before it. We from the mobile did not show anything visual because there is barely anything visual that has been done, but we informed the rest that we can contact APIs correctly, so as soon as the real API is up we can connect. The backend team has finished the backend skeleton and is ready to set it up to AWS so next week some real progress will probably be made.

One problem we had faced was that many of us believe that our schedule is a bit messed up. We changed time of meetings several times because it is very hard to make sure everyone can attend everytime. But the times we have decided on now should be fine for everybody so going forward it should be better.

<h1>Week 3</h1>

<h3>Monday 11 April</h3>

Online sprint planning with everyone. I am going to continue working with the app and we intend to finish all the setup this week. As we resolved the dependencies last week we should be able to implement it rather quickly. 1 More teammate will join the app work this week, he will focus mostly on UX meanwhile I will finish the setup stuff that was behind. The plan is finish the setup tomorrow (because I dont have time work on this project on mondays) and then start doing the views and finish them before the end of the week.

<h3>Tuesday 12 April</h3>

So we decided that I will not be doing the setup, rather I will just be reading documentation and working on some minor UX stuff.

<h3>Wednesday 13 April</h3>

Still reading documentation to understand how to correctly use MVVM structure for the project. Killian is working on implementation and is soon getting it done. I try to help whenever he needs help.

<h3>Thursday 14 April</h3>

MVVM structure is finished. Good job Killian. The retrospective was on discord because the lecture was on Zoom.  There were 1 person reported missing from the Mower-team. It was reported that we need a day where we decide upon some interface structure for the communication between mower-cloud-app.

<h1>Week 4</h1>

<h3>Tuesday 19</h3>

Monday was a red day so no sprint planning then. It was today instead and we decided to work on getting the connection complete this week. The app is ready to send http requests to the backend and the backend will be put up on a server this week. The mower will focus on it as well. Bluetooth will be the next step for next week.

<h3>Wednesday 20</h3>

Today I worked on merging the views to our new MVVM structure. The views was done in another branch on the side, so today when we were going to marge it was a bit of changes that needed to be done for conflicts. I worked on this with Killian and Ivin. After that we set it up so that we cleaned up a lot of code and are not using unnecessary code. It was a good day, we are ready for demo tomorrow where we will show the app and the views working correctly and being able to connect to API.

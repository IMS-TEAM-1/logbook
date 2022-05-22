Week 1: 

The first week was short because we got introduced to the course and the main objective of the course and what we supposed to achieve at the end of the course. It started with team introducing, we knew what we need to achieve but not how to start, so we laid everything out on the table, we started with setting up a Discord server for our team where we can have our off campus daily stand ups on, some Retrospective sessions and voice channels to help each others/ work together. The Discord tool is very crucial for communicating with the team and keep them updated even after work hours, where we can post any application status update and everyone on the group is able to see the message. We divided the Discord channel into two parts where the Robot/ Mower team can have their own chat and we at the Back-end/ Application have our own, this is made for stand ups, where its possible to have a collective meeting on Mondays with everyone on both groups on the same voice channel where we keep everyone updated and talk with the sub-team in our team. We also made a Trello room for our team where we divide the tasks into 4 sections, the first is “ToDo”, the second is “WIP” which stands for Work In Progress, the third section is “Testing” and the forth is “Done”. This structure is really appreciated because it shows what tasks needs to be done, what tasks we are working on and what tasks are done.


Week 2: 22 hours

We started our week with a collective meeting on campus, where the whole team sat down together and tried to come up with tasks that is needed to complete the application, once that was done, we went on and divided our groups into Robot/ Mower team and Back-end with Application we later had to divide us into sub teams so 3 went to the Back-end and 3 went to the Application.
To know what to do we had to ranks the difficulty of every task, and the one the ranked/ found the task to not be that difficult would take and work with that task, i ranked the majority of tasks to be semi easy, but i ranked the Design task to be the easiest since i have worked with Graphics and Design for a long time, so the Design task landed on me, but its not a easy task to complete and especially alone, so Yevve had to jump in and help me, but when in team discussed what the best tool to use to design, we ended up deciding to work with Figma, but even with all the years of expertise i had with Graphics and Design, so i had to start for the bottom, but i quickly found the User Interface to be easy to understand and very similar to Adobe XD which i'm most familiar with and quickly caught up and started Designing the different display views.


Week 3: 24 hours 

The week started with me starting working on the different views of the application on Android Studio in XML and Kotlin languages. I started with login screen with Email and Password text input fields with a Login button. The second view was the Mower status screen where it shows the connected mower and the status of connection if connected of not, it also shows the name of the mower with some helpful button at the bottom of the screen like Start/ Pause button where it starts the mower’s autonomous drive and with Pause button it pauses the drive, Timer button which takes the user to a list of alarms where the user can automatically start/ stop the Mower at specific times, the user can also create alarms by pressing add alarm button at the bottom, which leads the user to another screen that a user can choose a time and date and save it which would apear in the Timer list. The next screen was Map screen where it shows the map and the boundaries of the mower but i had hard time implementing it because i decided to use Google Map API. Next screen was the Controller screen where it hold all the button necessary to control the mower manually, button like forward, backward, turn left and turn right buttons. The next task in UI building i did was the navigation bar to ease the navigation in the app, which consist of 3 buttons, the first one is the Mower Status, the second one is Map and the third screen is the Controller.


Week 4: 23 hours

This week started with normal standup meeting on Monday where we decided what task we need to focus on during the week and who would do the tasks. 
I continued working on the UI with the rest of the screens. I started with the Path list which is a list of path preset that the mower can follow and shows on the Map screen. Both Path list and Timer list cannot be viewed without their own layout files where i specify every attribute to display and the look of them to later inflate that layout on the list which means that i assign the layout to the list and every Alarm/ Path will be looked that way.
At the end of the week i was done with programming the logic for screen navigation and time/ date.


Week 5: 19 hours 

once i was done with UI implementation it was time for Bluetooth implementation, starting with looking at Android documentation of how the Client side needs to be implemented, because the server side is being worked on from the Robot/ Mower team while me and Yevve work on Bluetooth Client implementation, After some digging we found what we were looking for, but a big problem was waiting for us, namely Bluetooth permissions, which didn't work what ever we tried to do. we tried everything we know, but nothing worked, we tried to write every permission that is needed manually but it didnt work, then we realized that we also need a function that displays a menu for the user to give permissions to use both Bluetooth and Location usage.  



Week 6: 20 hours
 
Me and Yevve continued to work on Bluetooth connection with the Robot/ Mower but without any luck, we still tried with Bluetooth connection and in a way that works with MVVM structure. which means that Views and ViewModels are separated. Views are the files which contains the XML code where the ViewModels are the files the containts the logic and a there was a error with Bluetooth code acquired by Android Documentation site, it needed to be in a View class to call a object called “context” which is basically a callback to the body of that view, so a work around had to be done and with some Google search i found that including Android ViewsModel into the class and calling an object called “getApplication” instead of context. 


Week 7: 16 hours

With all that working we still didn't manage to fully get a work around for the Bluetooth/ Location permissions but with some researching, we found out a Android package that helps with permissions which is called “EasyPermissions”, this package helped a lot with permissions because we created a object containing this function which can be called on any Bluetooth establishment function, functions like Bluetooth client connect function and Location permissions request function which is needed to use the Bluetooth sensor in a smartphone. i couldn't work much in the project because i got sick and couldn't do much at the end of the week. 

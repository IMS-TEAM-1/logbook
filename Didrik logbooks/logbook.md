# week 1

v.27 2022

The groups first meeting was on thursday (31/3).

In the meeting we decided our group structure of two teams with a scrum master in each, along with a product owner / team leader.
I am the scrum master for the backend-mobile team, and John is the scrum master for the mower team.

We split into teams and started to work on the database structure.
We have a good idea of how it should look, but some questions remain regarding what areas of communication are done via the api or bluetooth to the mower.
We can therefore not finalize our database structure.

A schedule was also set, where we meet on mondays at 9:00 to do a sprint planning session with the whole group.
We have internal team standups at tuesdays and wednesdays, and a demo at thursdays where the whole group is present.

Some tasks / stories where created in Trello but they need refinement.

# week 2

## sprint planning 04042022

We all met at school for the first sprint planning session.
Because a lot of discussion about what needs to be done was happening last week we all had a rough idea of what we needed to start working on.
We played planning poker to assign point to tasks to see how difficult we percieved them to be.
After that we split into smaller groups, two or three for each task, and started working on them.
My team made som progress on the backend architecture and structure, what packages to use etc.

During the day I set up the backend project with a three layered architecture with node.js.

- [commit](https://github.com/IMS-TEAM-1/backend/commit/021c731c8ceb79fcd91e0fae88c39d7aa5b9fbea)

## standup 05042022

Standup meeting online.
Everyone has progressed well with the task and we are on time schedule for this week. No hiccups.

During the day my team progressed with sending data through the different layers and exposing them as a local endpoint with rest-architecture.

- [commit](https://github.com/IMS-TEAM-1/backend/commit/3ebbde0f08f28149d1673651af8fc58fe3fc7711)


## standup 06042022

Standup meeting online.
The progress is solid and my subteam is done with the main task for this week and ready for demo / retrospective at thursday (tomorrow).


## retrospective 07042022

I met up with three others to work an halfhour before the meeting started.
We managed to debugg some code and later put it all within a docker-container for easier management of packages and startup scripts.
We also implemented nodemon for autorestart of the application whenever changes are made.

- [commit](https://github.com/IMS-TEAM-1/backend/commit/a3d5b722e7cacc87c7f74f1e0fe988cfee96480b)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/de643cc8dd4e07ddd50dd359084b983c419d49e6)

The retrospective was promising, all teams showed good progress and were all around happy with the week.
The main takeaway was our planning, we need to be more strict with the times we set to make sure everyone can be there.


# week 3

## sprint planning 11042022

We agreed on the retrospective to have it online.
Only two new tasks where added this week. We played (a loose version of) planning poker to assign the points for these cards and then again split into small subteams working on each card.

I worked later on in the day together with one teamate. 
He had implemented Knex and Bookshelf as ORM for communication between database and the api.
I started to work on bringing in the local instance of database into the docker instance, which I did get to work.
I did not however solve the communication of Knex, so the feature is not yet done.

- [commit](https://github.com/IMS-TEAM-1/backend/commit/15ac7f1a382e6462dcaa08c496978f24b26660d3)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/898d3a6c34d3d5a483566be54666343f8b4a6b26)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/cfe463890da765be508c84dab9f215f553e546c7)


## standup 12042022

Many had not yet started working on the project this week and instead focused on thesis work as a deadline is coming up. I had tried to add the database implemented using knex and bookshelf within a docker-container but did not succeed during this day. 
On wednesday I went on a trip and could not work on the project during this week.


# week 4

## sprint planning 19042022

Due to illness I could not attend our sprint planning (which was pushed from monday to tuesday due to "red day")


## standup 20042022

No real progress compared to yesterday as we all had a deadline for our thesis work this morning. I along with one more decided to together try and implement Google Vision API later this day.

Me and one other team mate met up online and started to work on the google vision api. 
The code itself was not difficult to implement, but we did not understand the authorization needed.
The steps detailed in the official documentation did not yield us any favorable results, so no more progress on this today.


## retrospective 21042022

The feelings in the group where rather good.
Some ups and downs during the week but not related to the project itself.

We in the backend team had some dependency issues that needed to be resolved during the weekend.
The goal for the next sprint is to do a connectivity test amongst all systems.


# week 5

## sprint planning 25042022

Like i mentioned in the retrospective, the goal for this week is to do an system wide connectivity test.
If the people working on mobile have time they shall also start looking into bluetooth connectivity.

To meet this goal we need to try and deploy the backend.
The dependency issues encountered last week are now fixed so now we just need to figure out how to deploy it.

Me and another team mate looked at it later this day but met trouble after trouble.
Because our system is managed with docker we thought we could simply delploy it using docker-hub, but because we are using two images it was eaiser said then done.
We did try to just deploy it using an Ubuntu instance, basically just a virtual machine but still could not access it.


# standup 26042022

A bit after we had our standup meeting one person in our team needed help with git.
I went to school to help him and together we managed to also deploy the backend correctly.
The issue was that we did not port forward the port the app used as endpoint.


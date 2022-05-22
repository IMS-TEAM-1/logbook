# week 1

hours worked: 20

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

hours worked: 20


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

hours worked: 10

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

Many had not yet started working on the project this week and instead focused on thesis work as a deadline is coming up. 
I had tried to add the database implemented using knex and bookshelf within a docker-container but did not succeed during this day. 
On wednesday I went on a trip and could not work on the project during this week.


# week 4

hours worked: 20

## sprint planning 19042022

Due to illness I could not attend our sprint planning (which was pushed from monday to tuesday due to "red day")


## standup 20042022

No real progress compared to yesterday as we all had a deadline for our thesis work this morning. I along with one more decided to together try and implement Google Vision API later this day.

Me and one other team mate met up online and started to work on the google vision api. 
The code itself was not difficult to implement, but we did not understand the authorization needed.
The steps detailed in the official documentation did not yield us any favorable results, so no more progress on this today.

We did merge our features from our `feature/database` branch into our main branch, along with writing some documentation.

- [commit](https://github.com/IMS-TEAM-1/backend/commit/2a2ea496ed036865f4e905a1d9f38830e4fc374d)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/4cf9239e25075fee64c7a7ca30347b8a66fbcc39)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/8f10ce1cc3f710935fc77e35166e8f3171306a48)


## retrospective 21042022

The feelings in the group where rather good.
Some ups and downs during the week but not related to the project itself.

We in the backend team had some dependency issues that needed to be resolved during the weekend.
The goal for the next sprint is to do a connectivity test amongst all systems.


# week 5

hours worked: 20

## sprint planning 25042022

Like i mentioned in the retrospective, the goal for this week is to do an system wide connectivity test.
If the people working on mobile have time they shall also start looking into bluetooth connectivity.

To meet this goal we need to try and deploy the backend.
The dependency issues encountered last week are now fixed so now we just need to figure out how to deploy it.

Me and another team mate looked at it later this day but met trouble after trouble.
Because our system is managed with docker we thought we could simply delploy it using docker-hub, but because we are using two images it was eaiser said then done.
We did try to just deploy it using an Ubuntu instance, basically just a virtual machine but still could not access it.


## standup 26042022

A bit after we had our standup meeting one person in our team needed help with git.
I went to school to help him and together we managed to also deploy the backend correctly.
The issue was that we did not port forward the port the app used as endpoint.

I also fixed some requests for users and mowers, updated our documentation and reworked the code from callbacks to async/await for cleaner looking code.

Callback example:

```js
manager.getAllMowers(function(data){
  respond.send(data)
})
```

async/await example:

```js
const data = await manager.getAllMowers()
respond.send(data)
```

- [commit](https://github.com/IMS-TEAM-1/backend/commit/d4f654a6bfa1361e68128d9a14ed3435fd80d7d1)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/227beb9b4811dd7842e6acb656d210c6826b3fcb)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/bbc1fb6fa9afba850ca7e1267326d1a8ae3bbfeb)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/08f13762b3165a9210c715b1a415e66807279913)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/5bf781db5c86123193904beba553e25e373fafd4)


## standup 27042022

Today I did do some error handling and skeleton code for images and locations.

- [commit](https://github.com/IMS-TEAM-1/backend/commit/d7640d75588ee60a7f9eb946ef2e1d54d6f1966a)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/77be5f273250d32f72bbd2416593a8c006373def)


## retrospective 28042022

The idea for this retrospective was to have a connectivity test, but the mobile team did not have the correct version of software on their computer and could therefore not participate.
We in the backend had also not published the last needed endpoints to the server.
Instead we talked about what we have done and what is left.

After the meeting me and another teamate sat down and fixed the rest of the endpoints in the backend along with error handling.

- [commit](https://github.com/IMS-TEAM-1/backend/commit/60171a26c373f74e01eb8e2df1ec4e51dfc46d15)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/ce3569fb642c31c73b27a5330591f2b9fbe7f1e9)


# week 6

hours worked: 20

## sprint planning 02052022

We discussed what is left to do and we are focusing on bluetooth connectivity and map visualization this week.


Some small tweaks are needed in the backend, but the main feature we are missing is the google vision api - image classification.
Other then that it feels like we are on schedule.

After the meeting I merged a branch with a lot of changes in to our main branch.
This means all endpoints and the logic for them is close to complete and up on the server ready for anyone to use.

- [commit](https://github.com/IMS-TEAM-1/backend/commit/0a8e96e03b75ea37eebfb37ae23999295f7730f1)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/f49de368a4d557e2b828cb5b6369dc1986388c51)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/9fc3200d97143e84ef76004dd22f2994366f1a44)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/e0dcc5c5789c1f2d3cd396a6e8729c99801db71a)

## standup 03052022

I did not do much work this day, fixed a typo after the mower team recognized that the backend crashed while they where trying to fetch a mower.

- [commit](https://github.com/IMS-TEAM-1/backend/commit/4fa857fb1de266061d0c01fcb491f4141cd4582b)


## standup 04052022

I met up with people from the mower team to help them questions about the API.
During this time I set up the skeleton code for how the image shall be created.

- [commit](https://github.com/IMS-TEAM-1/backend/commit/632f3810d9d0bc7294c4ba84d0078395529b8a61)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/3804042b91999171ef05c1291f2cf5d1f1e93320)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/8ec27bef4305971aa5c9fc24508be69893d77204)


## demo / retrospective 05052022

Today I also stopped by a bit earlier to help others.
During this time I went through our code and changed small things like more consistent namings and added more debugging logs.

We ran into a strange bug when the mower team made posts requests, and it happens to be that python cannot created nested objects. 
Our inital though was that the body of the post requests would look something like this, because we need the location to link the image to a location:

```json
{
  "image": {
    "image": "base64"
  },
  "location": {
    "x": 0,
    "y": 0
  }
}
```

But because python is unable to create nested objects, we had to change the requests body to look like this instead:

```json
{
  "image": "base64",
  "x":0,
  "y":0
}
```

Because of this I also sat down and updated our documentation, both the standard REAMDE.md file and our Api-docs.md file.

- [commit](https://github.com/IMS-TEAM-1/backend/commit/0e0bc0f2e7862baf477a9783375fd8c8d1222d7f)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/7f6e09f1c35fa7deae8bc299f54a999b59981fe3)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/0c39f794cdb576a49286961ede69bd04a0ce8859)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/90915cc8f9aeae3cde1d737fb6560e998a5c0bb9)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/f9d01630973b621e9acde7d30419be2f02e32550)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/f7eab471ca14ab8297e6d1a674c82e10170e137b)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/2aebe581d61381572dc000f02628d8a8c5b74943)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/063e4cc252dd957aaf2918abc98a7d57becd2a85)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/e4209c73ad36f91c3c54520a5efc8ad875543f73)


## sprint planning 09052022

We met up online the whole group and went over what we need to do.
What is left for the backend team is the google-vision-api.
The code for it and authentication is complete, we just need to look over it and test it.
The mobile team is focusing on bluetooth and the drawing of mower location this week.
The mower team shall focus on transmitting their position and any collision images to the backend.

We went over all milestones that we needed to complete and it is looking like we are on schedule.


## standup 10052022

Me together with one other teammate worked to finnish the Google Vision API implementation.
After this day it worked as intended but had not been tested thoroughly.
What is left is to clean up the code a bit and add some error handling.


## standup 11052022

Me together with the same teammate as before continued to work with google vision api. While it was working we had not tested it that much, but decided to still merge it into our main branch and push it up to the server for more testing.
We did also add some error handling by try catch to make sure that if the classification failed the server would still be up.

- [commit](https://github.com/IMS-TEAM-1/backend/commit/cbd9c9deb161bb7f699f41703bb6c003df4b6fb7)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/383624b370e902dae9cc177e7f1de2cbf755e7c1)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/c702e075000ae4ce6faf5e8b97b7ebd312694877)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/130515525c16edaeb7fd4c27c654033b211c07cd)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/86a69bef64ebe90bdff7119dd0ead741d9ef520d)


## retrospective 12052022

The mower team dislpayed a new feature where the mower runs a diagnostic test to make sure all modules works as intended.
They therefore requested that we add a state in the backend so that the mobile application can change it and therefore trigger the diagnostic state for the mower.
This shall be an easy fix but is pushed to next week as we still have some testing to do on google vision api.


# week 7

## sprint planning 16052022

We went over what is left to do.
Because google vision api was fixed last week what is left in the backend is adding an extra state for diagnostics that the mower can run, and testing to make sure everything works as intended.

The things needed for mobile team is drawing the map correctly and fixing sending commands via bluetooth for manual driving.

The things needed for mower team is connecting via bluetooth and sending commands coming from the mobile application to the aurdoino that sits on the mower.

I later this day did some documentation and added comments in our code.
I did also finnish the test script for image classification, where we connect to the backend and sends an image to see that it works properly.

- [commit](https://github.com/IMS-TEAM-1/backend/commit/7e6c7abf002556d5c5940c91eba358796fab4c83)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/76adb75eac7f0da193d84aa05895e1c8f4899927)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/62fe254ff5044462357ebe839abe360c7fc52469)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/a9616485e445aee24d452a708419ab2a30a349f9)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/39fedf7a1dce622b0b99dae4c896f5ae53ea0039)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/a95b4e5b9e4a11eda58085f2f51134cfdf432c01)


## standup 17052022

We went over what we had done and what we expect to finnish with today.
Drawing the map with the locations from the backend was the main focus point and I helped the person working on it later this day.
We managed to figure out how to scale the map according to the max x and y values present in the database, meaning our canvas for drawing is 500px and the max x value is 100, we have a scaling factor of 5 to make sure drawing of the map ends up scaling correctly.

During this time I tested the classification with different pictures.
How the api works is that it sends back an array of labels that all classify the image. Anyone of these is a correct classification, just in different ways. Example: Send an image with a fotball on grass with a blue sky backdrop. The API will respond with:

- sky
- fotball
- plant
- field
- etc..

The problem here is that there is no way of knowing in what order the labels are returned in, therefore we cannot decern which one actually represents the object we want. For now, we just take the first classication label and call it a day, but that unfortunely gives us the results "Sky" when we send in a fotball.

I feel like this is an issue with the API and not our code, and therefore will not put any more time into it.


## standup 18052022

Standard standup.
After the meeting I went to meet up most of our group at school to aid with questions and fix the remaining stuff in the backend.
We needed to rebuild our database when adding the new state `DIAGNOSTICS` which I did with some help from other teammembers.

The goal for tomorrow is to test all the functioning parts of the system, check our documentation and write a lessons learned document.
We aim to be as close to done as possible.

- [commit](https://github.com/IMS-TEAM-1/backend/commit/c64f6b9147f8de8fb45918464ac5095ab1cf6cd1)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/d4c3bf4f89df020321e979dfa3f39e54033cf3c8)
- [commit](https://github.com/IMS-TEAM-1/backend/commit/7b67ce8aa4fdc9eaee4b04d79066cfe1e61b6d11)

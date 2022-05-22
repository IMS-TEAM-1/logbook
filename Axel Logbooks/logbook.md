# Logbook
## Week 1

#### Hours: 20

This week we started the project work. Our first meeting was held on the 31st of march. We created teams and assigned different roles. The teams are divided into mower and
backend/mobile, although the backend and mobile are seperated on everything except the stand-ups. I was assigned to the backend team. We decided on Yevheniy as the project leader,
Didrik as the backend/mobile scrum master and John as the mower scrum master.

Altough my main position is in the backend team, I helped the mower team to build the robot. This consisted of assembling the robot and start it. We came across some problems,
such as a lack of batteries and a lack of a HDMI cable.

Furthermore, I worked with Didrik and Valentin on the database structure. We decided on using Knex and Bookshelf.

## Week 2

#### Hours: 20

We decided to have sprint planning every monday, stand up meetings every tuesday and wednesday as well as a retrospective/demo meeting every thursday. Our first sprint planning
was conducted on site since we figured it would be easier in the beginning. We wrote up some stories and estimated them using scrum poker. After we had estimated every task we
divided everyone to do certain tasks. I was assigned to do the API documentation which required the database structure to be complete. In addition to the API documentation I was
tasked to assist the rest of the backend team if needed.

During the retrospective we talked about what we had accomplished during the week. We did a retrospective board and a mood graph. We decided on doing this at the end of every week.
I think that the team overall worked very well this week. Everyone did their tasks and I feel like the progress made was good.

## Week 3

#### Hours: 20

This week most of the work and meetings were done online. Since the database structure was completed I was able to complete the API documentation. I worked together with one team
member on the mower team with getting the camera to work. The camera initially took picture in a too high resolution. We tried to fix this, although our Raspberry Pi was way too
slow, leading to this task taking a lot of time. We ended up switching to a more powerful Raspberry Pi. A lot of time has been spent on our thesis work this week. This lead to the
project's progress to not go forward as much as we would have liked.

## Week 4

#### Hours: 20

This week a team member and I started working on the image recognition API. We decided to use Google Vision API, which seemed to be a pretty straight forward API and a widely used
API. We initilized our project on Google and started to implement the functionality in the backend. It went pretty well code wise, altough we did eventually encounter a problem regarding
the credentials needed to authorize our requests. We went through Google's documention, but this was somewhat confusing because it sometimes seemed to contradict itself. An environment
variable was needed to authorize the requests, but after adding this, it still didn't recognize the credentials. This is something that we need to fix next week.

## Week 5

#### Hours: 20

This week I continued trying to fix the credentials issue with Google Vision API. It took some time and I asked asked around to see if anyone else had encountered the same issue.
After reading a lot of documentation and forum posts, as well as talking to others with the same issue I managed to fix the problem. We successfully sent a request and got a result
back. We sent an image of an onion through a URL and got the correct labeling back. The mower will send the image as Base64, so we tried to send a request using Base64. While trying
to fix this, I encountered another problem that needed to be fixed first. When testing the backend locally, nodeamon prevented the backend from starting. After fixing the nodeamon
problem I continued with trying to fix the Base64 problem. The server, understandably, thinks that the string is way too long. According to the Google documentation the request
is written correcty. I will have to continue with this during next week.

## Week 6

#### Hours: 20

I continued with the Base64 problem this week. I found a long thread on GitHub where multiple people had the same issue. According to another part of the Google documentation,
if sending a request with the key "content", the format should be a BitArray. The Google documentation altough seems to contradict itself here and this was acknowledged in the
thread. After altering the request structure a bit, as well as converting Base64 to a BitArray I managed to correctly send the the request and get a response. We decided to only use
the first label we get from the response. This label will be very general. For example, when sending an image of an onion, the first label will be "plant" or "vegetable". This is
because the API organizes the labels after a probabilty number. The API is 95% sure that the image depicts a vegetable, but only 78% sure that it depicts an onion. Since the API
does not organize its labels into sub-categories, we have to take the most probable label. I did however find a dataset from Google that were able to divide the labels into
sub-categories, and we might implement this to get a better label if there is time for it.

## Week 7

#### Hours: 20

This week we encountered a problem regarding sending and storing the images in the database. We wanted the images to be stored in the database to then be displayed in the app after
the mower encountered an object. However, storing the images outside the docker container on the server was not that easy. We tried to fix the problem, but figured since it is not
a requirement to display the image on in the app, we decided to only show the label. If we find more time, we will try to fix the problem. Furthermore, we had a problem with the
bluetooth connectivity. Most of the members from every team gathered to try to fix the problem.

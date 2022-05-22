# IMS GROUP 1 - Lessons learned

team members:

- Eric
- Didrik
- Alexander
- John
- Filip
- Yevheniy
- Sargis
- Ivin
- Axel
- Valentin
- Killian

## Bullet points

- Change hardware from old to new if available, as it is way faster and saves time :) (Rasberry Pi 0W to Rasberry Pi 4)

- Decide on a set meeting time and do not change it.

- While meetings on site are often better structured, the travel time to and from can be cumbersome for some. We decided to keep only the retrospective on sight.

- Decide on rules on how to handle people not present.
We never decided on any rules for it, but feel like it would be good to have some set ways of handling it.

- Come better prepared for integration tests.
There where many instances where we where supposed to have an integration test but could not because of bad preparation or small bugs.

- Focus on the task at hand.
There was talk about starting implementation of bluetooth already in week 4, but due to inproper task focus it got delayed until the last week.


## Main takeaways

`System wide tests`

More system wide tests that are better planned, and people are more prepared for them.
This is important to make sure that all new features introduced in a sprint works as intended.


`Work breakdown structure`

We decided to plan our project with a Trello board and use tickets for every sprint.
We feel like it would be a good idea to have a deeper planning session in the beginning and create a proper work breakdown structure to get an overview of the whole timeline for the project.
We did also stop using Trello and our Mira board in the end of the project, instead relied on communication between teams.
While this worked okay, it was not documented.



<h2>Time estimation of tasks</h2>

Sum of all Trello tickets is 207 points. The estimates are based on 20 hour work weeks. Overall the estimates were pretty accurate, there were however some outliers:

* Bluetooth **app** - 

  This was massively underestimated. We gave it an estimate of 13 points. However, with various bugs and errors, it took us several weeks to get it working and we finalized the last day (Sunday 22 May). 

* Serial communication **mower** -

  We faced some troubles with serial communication between the Arduino and raspberry pi, the data that was sent wasn’t accurate, we tried changing the baud rate which didn’t help. Instead we decided to change our serial protocol in a way that made the size of the data smaller which helped resolve the problem.

* Pi-camera  **mower** - 

  The Raspberry Pi uses a camera used when collision avoidance occurs. This camera, in some way, became defect. Either by shorted components or broken conductors between the Pi and camera sensor. This caused a lot of problems since this occured during the last system test. This resulted in a large amount of additional time spent with transferring the code, configurations and libraries to another Raspberry Pi. This took a lot of time and effort to get it up and running again.

* Handle encoder and gyroscope data **mower** - 

  The outlier which resulted in a reduced time than the estimate was to retrieve gyroscope and encoder data since it was already defined in existing MBlock libraries. The total time-difference was; a 7 down to a 2.

* Google vision api **backend** - 

  The credentials for verifying your account at google was complicated. The code was simple but the documentation was clear cut as to what response one would receive.

  


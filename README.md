
##Examination 3 - Monitoring monster

In this assignment, you will create a real-time layer above the web application you wrote in the previous assignment. The idea is to have a monotoring dashboard for athenticated users that shows events happening in the application. The application should also be published on a public server with a reversed proxy in-front of the node application.

>###Deadline
Thursday, March 17, 2016 7:00 AM 
###Submission Instructions
Submit your solution, by creating a release on GitHub named “v1.0″. In case of changes after creating a release, please increment the minor version number, i.e. “v1.1″, “v1.22", etc.

##Requirements

### The real-time application
The realtime layer should be a feature developed on the application you created in the previous assignment (Sticky snippets). The realtime application should be using the websocket protocol. The realtime feature should give authenticated users a possibility to get real-time notifications about the applications events. The miniumem requerments of events are:

* A users register a new account (the username should be notified)
* A user logs in to the system (the username should be notified)
* A user fails to log in to the system (the attempted username should be notified)
* A user creates a new snippet (a link to the new snippet should be notified)
* A user deletes a snippets
* A user starts editing a snippet (a link to a live editing view should be provided - see below)
* A user stops editing the snippet

When a user starts editing a snippet a user that watch the notifications should be able to join "a channel view" to watch the editing live. In this case only the user that starts editing the snippet should be able to edit and the others can just watch the editing process. Of course you can implement multiediting feature (more than one user editing the same snippet at same time) but that is not a requirement for this assignment.

The dashboard monitoring the event notifications should be designed in a appealing way for the user of the application

### Production of application
The application shall be running on a public web server in production enviroment. We recommend using "Digital ocean" which gives all students a own virtual public server but feel free to choose another provider. 

Other requirements are:

* The node.js application should have a reversed proxy (nginx) in-front 
* The application shall be running through HTTPS (no requirement of signed certifactes or that you need to buy a domain name)
* The code should be pushed to the live server through remote git pushes
* The node.js application should be running through PM2 
* You shall create a installations document that describes the installation process that you used. This shall be in md-format and provided in your repositorie.


## Extra features [optional]
Try to implement a own real-time feature (using the websocket). Examples can be:

* A chat presented on each snippet page where users can disques snippets.
* A whiteboard application presented on each snippet page
* A funny game hidden as a easter egg
* You probably have other more funny ideas...feel free to try them

## Examination
You will book a time for this and the oral exam which is 17/3 between 0830-1500. Availible times to book will be published on the course web page that week. The exam is graded U, G or VG.

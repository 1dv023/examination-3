
##Examination 3 - Into the wild

In this assignment, you will create a real-time layer on top of the web application you wrote in the previous assignment. The idea is to have a monotoring dashboard for athenticated users that shows events happening in the application. The application should also be published on a public server with a reversed proxy in-front of the node application.

>###Deadline
Thursday, March 17, 2016 7:00 AM 
###Submission Instructions
Submit your solution, by creating a release on GitHub named “v1.0″. In case of changes after creating a release, please increment the minor version number, i.e. “v1.1″, “v1.22", etc.
The application should be running on a public server and the URL should be in the README-file


##Requirements

### The real-time application
The realtime layer should be a feature developed on the application you created in the previous assignment (Sticky snippets). The realtime application should be using the websocket protocol. The realtime feature should give authenticated users a possibility to get real-time notifications about the applications events. The miniumem requerments of events are:

* A users register a new account (notification containing the username)
* A user logs in to the system (notification containing the username)
* A user fails to log in to the system (notification containing the  attempted username)
* A user creates a new snippet (notification containing a link to the new snippet)
* A user deletes a snippets
* A user starts editing a snippet (a link to a live editing view should be provided - see below)
* A user stops editing the snippet

When a user starts editing a snippet a user that watch the notifications should be able to join "a channel view" to watch the editing live. In this case only the user that starts editing the snippet should be able to edit and the others can just watch the editing process. Of course you can implement multiediting feature (more than one user editing the same snippet at same time) but that is not a requirement for this assignment.

The dashboard monitoring the event notifications should be designed in a appealing way for the user of the application

### Production of application
The application shall be running on a public web server in production enviroment. We recommend using "Digital ocean" which gives all students a own virtual public server but feel free to choose another provider. 

Other requirements are:

* The node.js application should have a reversed proxy (nginx) in-front 
* The application shall be running through HTTPS (no requirement of buying a domian name so self-signed certificate is OK)
* The code should be pushed to the live server through remote git pushes
* The node.js application should be running through PM2 
* You shall create a installation document that describes the installation process that you used to set up your production enviroment. This shall be in md-format and provided in your repositorie.


## Extra features [optional]
Try to implement a own real-time feature (using the websocket). Examples can be:

* A chat presented on each snippet page where users can disques snippets.
* A whiteboard application presented on each snippet page
* A game (maybe hidden as an easter egg)
* You probably have other ideas...feel free to try them

## Examination
You will book a time for this and the oral exam which is 17/3 between 0830-1500. Availible times to book will be published on the course web page that week. The exam is graded U, G or VG.

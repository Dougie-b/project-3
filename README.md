
# Esperanto

In one week as a group of four, we made an app for users to find teachers of various foreign languages or to sign themselves up as a teacher.


## Deployment

To view this project, please click on the following link

https://new-esperanto.herokuapp.com/
## Tech Stack

**Client:** React, Axios, Bootstrap, SCSS, CSS 

**Server:** Node.js, Express, Mongoose, MongoDB, Bcrypt, JsonWebToken

**Developlemt Tools:** Visual Studio Code, Insomnia, Yarn, Git & GitHub, Google Chrome dev tools, Cloudinary, Asana, Canva, Zoom, Slack, Heroku


## Planning

Once we had decided on an idea, we wireframed out what the wireframe should look like and mapped out how we wanted our Back-End to work.

We also made a board on Asana to help track our progress and so we didn't step on each other's feet when working!

![wireframe screenshot 1](https://i.postimg.cc/Kjmy5yrK/plan2.png)
![wireframe screenshot 2](https://i.postimg.cc/VsFwkdmX/plan3.png)
![wireframe screenshot 3](https://i.postimg.cc/5ypW7kns/plan4.png)
## Writing the Back-End

I took the lead on writing the Back-End; sharing my screen with the team on a Zoom call, we used Express and MongoDB.

We tested with Insomnia throughout the build.

We installed the necessary dependencies and set up a generic server to ensure we could get it running. Then we built in our schemas for users, teachers and reviews.

**Models**

The Teacher schema was our most complex with a large number of fields as well as a many to one relationship with the Review model so we could attach multiple reviews to each teacher.

The User schema had the usual necessary login details and a virtual field which we used to allow a user to edit and/or delete their own teacher profile. 

We used Cloudinary to upload images and convert the url into a string to store in the database & we used bcrypt to hash the users' password

![Teacher model](https://i.postimg.cc/nVmyXMx3/teacher-model.png)

![User model](https://i.postimg.cc/W15KBkm1/user-model.png)

**Authentication**

We used JSONWebToken to create the controller that would check if the user was valid, then wrote a secure route to verify user identity.

![Authentication 1](https://i.postimg.cc/L8vKm7SR/authentication1.png)

![Authentication 2](https://i.postimg.cc/wBbCmm3G/authentication2.png)

**Controllers and Routes**

We wrote requests for each endpoint we needed for the Front-End using GET, PUT, POST, DELETE controller requests.

Then we determined which routes would require authentication and if so, also a secure route and added it into the middleware where necessary.

![Routes 1](https://i.postimg.cc/sDRt7yDs/routes1.png)


![Routes 2](https://i.postimg.cc/sx5qqHmk/routes2.png)

## Writing the Front-End

First we created a React app and hooked it up to our database and created various component pages we had planned to include and divided up the pages among us, however we all ended up assisting with each other as individuals had their strengths, so we used them!

**Home Page** 
As well as the standard information displayed on the home page I made a function that I was proud of & amused by that would use state combined with a Get request to count the total number of languages taught on our website and display that value on the Home Page and it would automatically update if there was a new language added!

![Language counter](https://i.postimg.cc/hGjFvr4m/countlanguages1.png)

![Language counter](https://i.postimg.cc/SN7HG5J8/countlanguages2.png)

**List of Teachers**

The next page was a list to display all of our teachers with various filter options.

![Teacher list 1](https://i.postimg.cc/MTCgsJ70/teacherlist1.png)

![Teacher list 2](https://i.postimg.cc/CKdtSxJH/teacherlist2.png)

![Teacher list 3](https://i.postimg.cc/QCZnQkD0/teacherlist3.png)

**Teacher Profile**

We made a page to display detailed information about an individual teacher including any previous reviews left by other users as well as the option to leave your own review.

We added the functionality for a teacher to be able to edit their own teacher page or even delete it should they so desire.

![Teacher Profile 1](https://i.postimg.cc/FHr8CZL6/teacherpage1.png)

![Teacher Profile 2](https://i.postimg.cc/bJtBSV7Z/teacherpage2.png)

**Adding images with Cloudinary**

When a user decides they would like to create a teacher profile they are required to add a picture. We made a component to post a request to Cloudinary to get a URL for the image we sent to upload.

![Cloudinary](https://i.postimg.cc/hjzHbtdP/cloudinary.png)

## Styling

In this project we used some Bootstrap elements to help us achieve a certain professional looking aesthetic.

It also was useful in terms of making the website responsive and still looking sweet on a mobile. 

I was extremely pleased with how the site came out looking, all the team has Ali to thank for his excellent sense of styling.
## Post Project Thoughts

This was the first time I built a Back-End so we didn't want to make it too complex, kept it fairly simple and very useable. It was done within the first couple of days which put us nicely ahead of schedule. Next project I think I'll push myself in terms of making a more complex database and using more relationship types.

We really had to learn to communicate effectively what we were each working on and when to do our merges to avoid having any conflicts. Merge parties are the way forward!

Much much googling! Had to really dig into various documentation to learn and apply new concepts that made our lives easier. Some people write really really bad documentation :(

Honestly I'm super stoked about how it turned out, our very first full stack web app and it looked and behaved exactly how we'd initially planned it to. Great success!

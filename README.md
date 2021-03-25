# Academy Training

## Getting Started 🚀

_This guide will help you to know how Academy works and what you need to run the different environments_

### Glossary 📓

* CEB = CE Broker
* EC = EverCheck
* LMS = Learning Management System
* Course flow = Course content view (Licensee)
* Course Builder = Create and edit course view (Provider)
* Monorepo = Repository that includes several projects within it
* Scaffolding = 
* AWS = Amazon Web Services

### Technologies Involved 🛠️

* Node + Express
* Jest
* Styled components
* Microservices
* Api Rest
* Mongo Db
* AWS
* React

### Prerequisites 📋

* [MongoDB](https://www.mongodb.com/try/download/community) - for Database
* [Postman](https://www.postman.com/) - for API
* [Robo 3T](https://robomongo.org/) - for DB Management

## First phase 1️⃣

_In this part of the training you are going to get involve with the product and understand how it works_

### Topics

* Small talk about CEB and LMS
* Show test sites: CEB, Course builder and Course flow
* Scaffolding, monorepo, tecnologies concepts
* Ways to run sites: independent or docker

_Clone repositories run them and use .env files_

### How to run the sites (Practice) 📝

_go to LMS [repo](https://github.com/cebroker/lms) clone and follow the steps_

1. Ask for .env files for API / Course Builder / Course Flow projects and add them to the appropiate folders

2. Add Hosts

* In each .env file you are going to find HOSTS variable like 'COURSE_BUILDER_URL' or 'COURSE_STUDY_URL'
* Add these urls to [HOSTS](https://www.dalendesign.com/webpress-blog/webmaster-tools/edit-hosts-file-in-mac-terminal/) file.

3. Connect MongoDB

- When you try to to connect MongoDB with ```mongod``` and doesn't work, maybe this [article](https://stackoverflow.com/questions/58283257/mongodb-cant-find-data-directory-after-upgrading-to-mac-os-10-15-catalina) could help you

4. Run the Course Builder site

- If you followed all the [LMS](https://github.com/cebroker/lms) steps correctly:

* You are going to see an empty window, to resolve this you need to add the 'clientCourseId' at final of the url
* Use Robot 3t to find it, 'clientCourseId' is on 'courses' table
* finally you can add the 'clientCourseId' at the end of the url /clientCourseId

for example

```
http://course.builder.dev.evercheck.com:3000/1c5cd9c3-c6ae-4405-9e5c-712c71dbc643
```

6. Run the Course flow site

- If you followed all the [LMS](https://github.com/cebroker/lms) steps correctly:

* You are going to see an empty window, to resolve this you need to add the 'clientLicenseeId' at final of the url
* Use Robot 3t to find it, 'clientLicenseeId' is on 'licensees' table
* finally you can add the 'clientLicenseeId' at the end of the url /clientLicenseeId

for example

```
course.study.dev.evercheck.com:3000/75f9e09b-9645-4928-b010-a871bf5bbf07
```

## Second phase 2️⃣

_In this pahse we are going to be getting involve with LMS diagram_

### Topics

* Arquitecture with [diagram](https://user-images.githubusercontent.com/13154205/64726528-77b75100-d49c-11e9-9ed8-4b2106d55f97.png)
* Authentication flow
* Forks
* Client Repos
* .env file
* Code Injections like way to adapt LMS for each client

- LMS works like monorepo cause it have more than one project inside

These projects are:

* Course builder: course builder dashboard for providers / teachers
* Course flow: courses view for licensees

_LMS is the CORE platform while CE Broker and EverCheck consume LMS resources through code injections that serves to modify LMS core to manipulate the information on way they need it instead of modify original LMS_

### How to run the sites (Practice)📝

_Like in the first phase you have to run the projects but in this case forks projects_

_For each project you need to run API / Course Builder / Course Flow_

#### Forks Projects

* [CE Broker](https://github.com/cebroker/ceb-now)
* [EverCheck](https://github.com/cebroker/ec-lms)

_if you followed the steps correctly at this point you should have run 9 projects, 3 projects per repo_

_Those projects are: API | Course Builder | Course flow_

_The repositories we have cloned are: lms | ceb-now | ec-lms

## Third phase 3️⃣

_In this pahse we are going to be getting involve deeply in media api section of LMS [diagram](https://user-images.githubusercontent.com/13154205/64726528-77b75100-d49c-11e9-9ed8-4b2106d55f97.png)_

Media Api: Api encargada de convertir los videos y contenido multimedia para su menor consumo posible y poder proveerle dicho almacenamiento a LMS CEB y EC. Sin correr esta api sera imposible adjuntar archivos multimedia al course builder.

* Media Api: Api in charge of convert media content into a specific format for the lowest possible consume and be able to provide this storage to LMS CEB and EC.
* Without Media Api running it will be imposible to add media content into the course builder

### How to run api media (Practice)📝

* In this case we only run api projects without course builder and course flow

Api media repos:

[Media Api](https://github.com/cebroker/media-api)
[CEB Media Api](https://github.com/cebroker/ceb-media-api)
[EC Media Api](https://github.com/cebroker/ec-media-api)

* Run api media and lms project completely
* Try to add media content to course builder

_if you followed the steps correctly at this point you should have run 12 projects considering 3 media api projects_


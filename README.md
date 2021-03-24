# Academy Training

## Getting Started 🚀

_This guide will help you to know how Academy works and what you need to run the different environments_

### Glossary 📓

* CEB = CE Broker
* EC = EverCheck
* LMS = Learning Management System
* Course flow = Course content view (Licensee).
* Course Builder = Create and edit course view (Provider).
* Monorepo = Repository that includes several projects within it.
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
)

## First phase 1️⃣

_In this part of the training you are going to 

go to LMS [repo](https://github.com/cebroker/lms) and clone.

### how to run the sites 📝

1. Ask for .env files for API / Course Builder / Course Flow projects and add them to the appropiate repositories.

2. Add Hosts

* In each .env file you are going to find HOSTS variable like 'COURSE_BUILDER_URL' or 'COURSE_STUDY_URL'
* Add these urls to [HOSTS](https://www.dalendesign.com/webpress-blog/webmaster-tools/edit-hosts-file-in-mac-terminal/) file.

3. Run the database

```
mongod
or
mongod --dbpath ~/data/db
```

If you want to play with some test data locally, to generate some seeds in the database run:

```
npm run seed
```

4. Run the API

* Go to "/packages/api"

* To install packages dependencies and execute the API locally run:
```
npm install
npm run start-dev
```

* To fill data

5. Run the Course builder site

* Go to "/packages/apps/course-builder"

* To install packages dependencies and launch the project:

```
npm install
npm start
```

* You are going to see an empty window, to resolve this you need to add the 'clientCourseId' at final of the url
* Use Robot 3t to find it, 'clientCourseId' is on 'courses' table
* finally you can add the 'clientCourseId' at the end of the url /clientCourseId

for example

```
http://course.builder.dev.evercheck.com/1c5cd9c3-c6ae-4405-9e5c-712c71dbc643
```

6. Run the Course flow site

* Go to "/packages/apps/course-flow"

* To install to install packages dependencies and launch the project run:

```
npm install
npm start
```

* You are going to see an empty window, to resolve this you need to add the 'clientLicenseeId' at final of the url
* Use Robot 3t to find it, 'clientLicenseeId' is on 'licensees' table
* finally you can add the 'clientLicenseeId' at the end of the url /clientLicenseeId

for example

```
course.study.dev.evercheck.com/75f9e09b-9645-4928-b010-a871bf5bbf07
```

## Second phase 2️⃣

_LMS works like monorepo porque en un solo repositorio encontramos la api y ambos modulos del las que son dos proyectos distintos pero se alojan dentro del mismo repositorio_

Estos proyectos dentro de los son:

Course builder: el constructor de cursos para los providers / teachers
Course flow: es la visualization de los cursos para los licensees

LMS es el core de la plataforma mientras que cebroker y evercheck consumen sus recursos mediante code injections que sirve para modificar el core (lms) para manipular su información de la maneras en que lo requieran sin modificar directamente el core (lms)

## Third phase 3️⃣

Media Api: Api encargada de convertir los videos y contenido multimedia para su menor consumo posible y poder proveerle dicho almacenamiento a LMS CEB y EC. Sin correr esta api sera imposible adjuntar archivos multimedia al course builder.


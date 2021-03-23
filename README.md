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

## First phase 1️⃣

go to LMS [repo](https://github.com/cebroker/lms) and clone.

### how to run the sites 📝

1. Ask for .env files for API / Course Builder / Course Flow projects and add add them to the appropiate repositories.

2. Add [HOSTS](https://www.dalendesign.com/webpress-blog/webmaster-tools/edit-hosts-file-in-mac-terminal/)

* In each .env file you are going to find HOSTS variable like 'COURSE_BUILDER_URL' or 'COURSE_STUDY_URL'

2. Run the database

```
mongod
or
mongod --dbpath ~/data/db
```

3. Run the API

* Go to "/packages/api"

* To install packages dependencies and execute the API locally run:
```
npm install
npm run start-dev
``` 

4. Run the Course builder site

* Go to "/packages/apps/course-builder"

* To install packages dependencies and launch the project:

```
npm install
npm start
```

5. Run the Course flow site

* Go to "/packages/apps/course-flow"

* To install to install packages dependencies and launch the project run:

```
npm install
npm start
```

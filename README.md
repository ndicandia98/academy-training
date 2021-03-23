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

### Technologies Involved 🛠️

* Node + Express
* Jest
* Styled components
* Microservicios
* Api Rest
* Mongo Db
* AWS
* React

## First phase 1️⃣

go to LMS [repo](https://github.com/cebroker/lms) clone and follow the steps.

_how to run the sites resume_

1. Ask for .env files for API / Course Builder / Course Flow projects and add add them to the appropiate repositories.

2. Run the database

```
mongod
or
mongod --dbpath ~/data/db
```

3. Run the API

* Go to "/packages/api"

* To install packages dependencies run:
```
npm install
``` 

* To execute the API locally run:
```
npm run start-dev
```

4. Run the Course builder site

* Go to "/packages/apps/course-builder"

To install packages dependencies run:

```npm install```

To launch the project run:

```npm start```

5. Run the Course flow site

* Go to "/packages/apps/course-flow"

To install to install packages dependencies run:

```npm install```

To launch the project run:

```npm start```



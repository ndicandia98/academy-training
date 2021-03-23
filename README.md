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

First phase 1️⃣

go to LMS [repo](https://github.com/cebroker/lms) clone and follow the steps.

_how to run the sites resume_

1. Ask for .env files for API / Course Builder and Course Flow projects.

2. Run the database

```
mongod
```

If doesn't work try: 

```
mongod --dbpath ~/data/db
```

3. Run the API

* Go to "/packages/api"

* Run to install packages dependencies:
```
npm install
``` 

* Run  to execute the API locally.
```
npm run start-dev
```


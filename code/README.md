# Implementation Mind Map

## Prerequisites
- **Node Modules & Packages**
  - `sudo npm install -g node-modules`
  - `npm install express`
  - `npm install pg`
  - `npm install bcrypt`
  - `npm install ejs`
  - `npm install moment --save`
- **PostgreSQL Setup**
  - **Add PostgreSQL Repository**
    - `sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'`
  - **Install Key & Update**
    - `wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -`
    - `sudo apt-get update`
  - **Install PostgreSQL**
    - `sudo apt-get -y install postgresql`

## Run
- **Database Setup**
  - Configure `database.js`
  - Create a database named "restaurant"
- **Run Application**
  - `node app.js` in terminal

## App Link
- Server available at [http://localhost:3000/](http://localhost:3000/)

## Implementation Details
- **Architecture**: MVC Pattern
  - **Models**: Handle DB queries
  - **Controllers**: Act as middleware
  - **Views**: Serve frontend
- **Additional Documentation**
  - Details in PPT and report

## Error Handling
- **Database Lock Error**: `/var/cache/debconf/config.dat is locked by another process`
  - `sudo fuser -v /var/cache/debconf/config.dat`
  - `sudo kill PID`
- **Other Errors**: Logged to console using `.catch(err -> console.log(err))`

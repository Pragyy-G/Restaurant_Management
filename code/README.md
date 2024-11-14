# Implementation

## Prerequisites:  
- sudo npm install -g node-modules  
- npm install express  
- npm install pg  
- npm install bcrypt  
- npm install ejs  
- npm install moment --save
  
If you don't have postgres installed:  
- sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'  
- wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -  
- sudo apt-get update  
- sudo apt-get -y install postgresql   
 
## Run  
SET UP the database.js file, Create a database called "restaurant"  
Run node app.js on the terminal  

## App Link:  
- The server will be live at: http://localhost:3000/  

## Implementation Details:  
- We have used the MVC architecture since it simplifies the system by separating into models (for querying the DB), controllers (middleware) and views (frontend).
- Rest can be found in the ppt and the report.  

## Error Handling:
In case you get an error:  DbDriver "config": /var/cache/debconf/config.dat is locked by another process: Resource temporarily unavailable  
- sudo fuser -v /var/cache/debconf/config.dat  
- sudo kill PID 

All other errors will be displayed on the terminal since we have used *.catch(err->console.log(err))*

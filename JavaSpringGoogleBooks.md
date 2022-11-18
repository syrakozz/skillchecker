[Home](README.md)
# Java spring boot skill checker

Write a rest api program using spring boot to connect to remote google books library and get from the first 1K books the count of books per author and store it in a database
The data structure is as follows:

* Number of books under study
* Time
* Sync datetime
  
<table>
    <tr>
        <th>Author</th>
        <th>Number of books</th>
    </tr>
    <tr>
        <td>(ex) Test Author</td>
        <td>4</td>
    </tr>
</table>

> For information about books apis read [this](/GoogleBooksConcept.md)

The read books API will be internal and not exposed to the clients, make sure that you authenticate before connecting to google

The read books API shall be fetching data periodically using a time interval set in the config of spring boot

**Write an api to fetch the data from the database and display it with the last synchronization date from google API**

The solution need to be able to deploy on a docker container using docker files and docker-compose yaml 


> **TIPS**

you can create a database using one of the below
* https://remotemysql.com/
* https://www.elephantsql.com/
* https://www.heroku.com/postgres
* https://heliohost.org/
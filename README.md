# springboot-restwebservice-manytomany-relationship
Spring boot rest web service application for many many relationship.

Database stucture for channel subscriber many to many relationship.
*******************************************************************

create table channel (cid integer(9) not null AUTO_INCREMENT primary key, name varchar (20));



create table subscriber (sid integer(9) not null AUTO_INCREMENT primary key, name varchar (20));

create table channel_subscriber(cid integer(9) not null, sid integer(9) not null);


There are following requests which are helpful in making data for subscriber and channel and making many to many relationship with one another.
***********************************************************************************************************************************************

For creating channel:

POST: http://localhost:8080/channel/

{
  "name" : "Discovery"
}

----------------------------------------------------------
For creating subscriber:

POST: http://localhost:8080/subscriber/

{
  "name" : "Ranjan"
}

----------------------------------------------------------
For gettting the list of all channels:

GET: http://localhost:8080/channel/

----------------------------------------------------------
For gettting the list of all subscribers:

GET: http://localhost:8080/subscriber/

----------------------------------------------------------
For adding existing particular channel to subscriber:

POST: http://localhost:8080/channel/<sid>

{
  "name" : "Zee News"
}
----------------------------------------------------------
For adding existing particular subscriber to channel:

POST: http://localhost:8080/subscriber/<cid>

{
  "name" : "Ranjan"
}

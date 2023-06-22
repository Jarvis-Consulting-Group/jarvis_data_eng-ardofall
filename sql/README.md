# Introduction

# SQL Queries

###### Table Setup (DDL)
create table cd.members(
  memid INTEGER not null, 
  surname VARCHAR(200) not null, 
  firstname VARCHAR(200) not null, 
  address VARCHAR(300) not null, 
  zipcode INTEGER not null, 
  telephone VARCHAR(20) not null, 
  recommendedby INTEGER, 
  joindate TIMESTAMP null , 
  constraint members_pk primary key (memid), 
  constraint fk_members_recommendedby foreign key (recommendedby) 
  references cd.members(memid) on delete set null,
);
create table cd.bookings(
  bookid INTEGER not null,
  facid INTEGER not null,
  memid INTEGER not null, 
  starttime TIMESTAMP not null, 
  slots INTEGER not null,
  constraint bookings_pk primary key (bookid),
  constraint fk_bookings_facid foreign key (facid) references cd.facilities(facid),
  constraint fk_bookings_memid foreign key (memid) references cd.members(memid)
  );
create table cd.facilities(
  facid INTEGER not null, 
  name VARCHAR(100) not null, 
  membercost numeric not null, 
  guestcost numeric not null, 
  initialoutlay numeric not null, 
  monthlymaintenance numeric not null, 
  constraint facilities primary key (facid), 
  );

###### Question 1: Show all members 

```sql
SELECT *
FROM cd.members
```

###### Questions 2: Lorem ipsum...

```sql
SELECT blah blah 
```



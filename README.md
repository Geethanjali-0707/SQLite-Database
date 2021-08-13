# SQLite-Database
database created by python and sqlite
1. create a connection:
         
     Import mysql.connector
             mydatabase=mysql.connector.connect(
   host="hostname",uesr="username", password="pwd")

print (mydatabase)



2. create a database:

import mysql.connector

mydatabase= mysql.connector.connect(
  host="localhost", user="user name",password="pwd")

mycursor = mydatabase.cursor()

mycursor.execute("CREATE DATABASE mydatabase")




3. create a table:

import mysql.connector

mydatabase = mysql.connector.connect(
  host="localhost",user="user name", password="pwd",database="mydatabase1")

mycursor = mydatabase.cursor()

mycursor.execute("CREATE TABLE movies (name VARCHAR(200), year of release VARINT(4), director VARCHAR(200), actor VARCHAR (200),actress VARCHAR (200), language VARCHAR (200))")




4. insert values into the  table:

import mysql.connector

mydatabase = mysql.connector.connect(
  host="localhost", user="user name", password="pwd",database="mydatabase1"
)

mycursor = mydatabase.cursor()

sql = "INSERT INTO movies(name,language, year of release, director, actor,actress, ) VALUES (%s, %s,%s,%s,%s,%s)"

val =[ ("bigil",tamil,"2020 ","Atlee Kumar","Vijay","Nayanthara")

("Harry Potter","english",2001,"Chris Columbus","Daniel Radcliffe","Emma Watson")

("Fidaa","telungu",2017,"sekhar kammula","varun tej","saaipallavi",)
("Dhoom","Hindi","2004","sanjay gadvi","Rithik Rosan","Iswariya Raai")
]

mycursor.execute(sql, val)



print(mycursor.rowcount, "details added into the movies")




5. Querying data from movies table:


import mysql.connector

mydatabase = mysql.connector.connect(
  host="localhost", user="user name",
  password="pwd",database="mydatabase1")

mycursor = mydatabase.cursor()

mycursor.execute("SELECT name,Language, year of release, director, actor, actress FROM movies")

Movies details= mycursor.fetchall()

for x in Movies details :
  print(x)




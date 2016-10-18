1. Install mysql server. Take note of the temporary password
2. Add to the ~/.bash_profile: export PATH="/usr/local/mysql-5.7.16-osx10.11-x86_64/bin:$PATH"
3. Start the server mysql -u root -p
4. Update the password to: ALTER USER 'root'@'localhost' IDENTIFIED BY 'justinmysql';
5. Create the test database: create database test;
6. Use the test database: use test;
7. Create the person table: create table person ( pId BIGINT Primary Key, personname varchar(32), personAge float);
8. Insert into the person table: insert into person values (1, 'justin', 35);
9. Build the project: mvn clean install
10. Remove the Tomcat ROOT folder
10. Copy the war file into <Tomcat directory>/webapps
11. Restart tomcat
12. Make a call to http://localhost:8080/SpringDataRestExample/api/persons

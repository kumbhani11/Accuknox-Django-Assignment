![image](https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/72d8e21c-13da-440e-acfa-294e40630617)# AccuknoxSocial

## Let's get started
This is a social media application(Backend) built with Django and Django Rest Framework

### Features/Functionalities
- Create User
- User Authorization
- Add Friends
- View Friends
- Search for Users

### Installation
- clone the repo from your Terminal/cmd using the command: ```https://github.com/kumbhani11/Accuknox-Django-Assignment.git```
- Make sure you have Docker installed in your local system.
  
If you do not have Docker installed you can run the same in your local system with the commands below.
- Create a virtual Environment
- Install the required libraries and modules: ```pip3 install -r requirements.txt```
- Populate the .env file with the configuration for PostgreSQL.
  Example:
  ```
  ENGINE = django.db.backends.postgresql
  DB_NAME = accuknox_social_db_local
  DB_USER = postgres
  DB_PASSWORD = password
  DB_HOST = localhost
  DB_PORT = 5432
  ```


- Also, Create a new DB for the same.
- Run the migrations command
  ```python manage.py makemigrations```
  ```python manage.py migrate```
- Run the Server: ```python manage.py runserver```

With Docker installed
- Run the Command: ```docker compose up -d db```
- Create the Build: ```docker compose build```
- Run: ```docker compose up```
- Open Docker Desktop and look for the running service under db you will see the container ID copy that and Go to your Terminal and hit command: ```docker inspect <container_id>``` (Replace <container_id> with the Container ID you have copied and scroll down to fetch the IP Address.
  <img width="1440" alt="263660083-b2c8c1b9-8022-43d7-bf04-0c8fcb6bf4a6" src="https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/1191a3ab-94ed-4690-a088-91725f95f5f5">
![image](https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/35ab46a0-e270-4006-80b3-4cdcf2b38181)


- Now Open your Browser and go to [localhost:5050](http://localhost:5050/) and login wiht the credentials mentioned under pgadmin section of the docker-compose.yml file and create a new connection with the details mentioned under the db section of the docker-compose.yml file and in the host name enter the IP Address you fetched
 ![image](https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/5322649e-8446-422e-b5e4-e962d2b3ad85)

![image](https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/a08b0c70-d1bf-406d-a826-1e27b80aa46d)


 - You can see all the tables populated during migration
![image](https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/c2f412fb-f077-485d-a568-d96e16e5f6b0)


Once you see the app is up and running you can play along with it.

## The IDs required in Adding Friends (User Id) and Accepting/Rejecting Friend Request (Friend Request ID) can be fetched from the Database via SQL queries

## Load the [Postman json](https://github.com/kumbhani11/Accuknox-Django-Assignment/blob/main/Accuknox%20Social.postman_collection.json) collection in Postman and you can work along with the urls 

## Functionalities
1) Sign Up
![image](https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/56b4d2c3-dec5-444b-84fe-f0a8391678f2)


2) Login
![image](https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/fb3640e8-03ce-49db-86cc-e0b2fa70ba7c)


Once you login with the right credentials(case insentivity handled)
A Token will be generated and that token needs to be added to the Headers Section
with key as ```Authorization``` value as ```token <token>```
This ensures the user is authenticated and only Authenticated users can access the APIs below.

![image](https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/6060560c-22dc-4047-9a89-88f65be97ed0)


3) Log Out
![image](https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/a83f5d40-fb03-458b-b47e-f8456cff231c)



4) Add Friend
After loading a number of users you can also send friend requests to them and add them to your friends list subject to acceptance of your friend request by the recipient.
Cannot send more than 3 requests per minute
![image](https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/33529d15-bc66-48ae-8876-9fd5ce1b89bf)



6) Pending Friend Requests
![image](https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/427c774a-92ea-4114-870a-ac5dc7bcf393)


   - Accept Friend Request
![image](https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/5152a5e2-73a3-4ff1-9d41-9faadde7602c)


   - Reject Friend Request
![image](https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/ed69e69d-aa3f-4aa6-ac7b-a81bde9dbbb4)


   - Unauthorized Action
![image](https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/c64fcc2e-3d04-417e-9822-55d29856096a)


7) View Your Friends (Pagination Applied)
![image](https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/6848b9cd-5a70-40fd-8373-82d0499a59ca)


8) View All Users and Search for Users
  - All Users
![image](https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/3a3bdf72-be48-480e-92fa-3fad48e5eee5)


  - Search Users
    - Search users containing a specific letter like 'j'
![image](https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/99dba6ab-2f84-46ff-8202-73da875de3cb)


    - Search with user's email (case insensitive)
![image](https://github.com/kumbhani11/Accuknox-Django-Assignment/assets/51017576/ab0accef-13c0-403f-a807-68c79290bd8d)


    
























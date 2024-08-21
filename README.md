# Authentication and Authorisation

## Introduction

Authentication and authorisation both are crucial elements of web security. Although they are often used together, they are serve distinct purposes in web security and must be carefully managed.

## Difference between Authentication and Authorisation

* Authentication: To authenticate a user. For instance, during login the user enters some credentials such as username and password that are matched against system records. If the credential matches then he is authenticated and user uses system. Imagine that authentication as the one type of key for opening a door to the system.

* Authorization: Once authenticated, authorization will determine what all you can perform as the user. This is the process of allowing or denying access to resources on or within a system. For instance, assume a user is already authenticated and logged in users does not have access to delete someone else's account unless they are an admin or special privileges. Think of it as a key to different rooms in the system. You can't access the room you are not authorised to.

## Why Deleting a User After Authentication is a Bad Idea
It is a bad idea to delete a user account only by authentication, without proper authorization. Here's why:

* Security Risks: Anyone logged in could maliciously delete accounts from the system. A grudge-holding user could delete all of the accounts owned by users, which would result in data loss and broken platform trust.

* No Accountability: If there is nothing to restrict who can run such a crucial operation like deleting someone's account, it will wreck havoc in the system. This will cause misuse of the delete functionalities either by mistake or interference intentionally.

* Allowing End Users to Bypass the Principle of Least Privilege: The principle of least privilege is that users should have only as many permissions as they need in order to do their job. Deleting other users is not a role for all the users.


# Running the Application
1. Clone the App in your Local environment:
```bash
git clone https://github.com/AdNarayan07/authentication-and-authorisation-with-expressjs
```
2. Go to back-end directory, install the dependencies:
```bash
cd authentication-and-authorisation-with-expressjs/back-end
npm install
```
3. Add a `.env` file in the back-end folder:
```env
TOKEN_KEY = "StackUpAuthenticationProject123!";
PORT = 4001;
```
4. Install "Live Server" and "Sqlite3 Viewer" VS Code extenstion
5. Go to `web-front-end\pages\index.html` file and the click "Go Live" on bottom right, the frontend Application will start running.
6. Run the backend server (while still inside the back-end directory):
```bash
node app.js
```
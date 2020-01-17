--- 
published: true
title: Back End Capstone
layout: post
category: programming, Nashville Software School, SWGOH Counters
tags: 
- programming
- Nashville Software School
- SWGOH Counters
---

### What is SWGOH Counters?
A Companion app for the mobile game Star Wars: Galaxy of Heroes, SWGOH Counters, built with React.js and using the Google Sheets API as a server. This application is used as a reference guide for players to look up which teams are best to use against teams they are battling. This app currently has an average of over 45,000 users and 420,000 pageviews per month.

### Why this project for my Back End Capstone?
I built SWGOH Counters as my Front End Capstone at Nashville Software School.  Due to its popularity in the game's community, I wanted to take the opportunity to develop the server side.

### Goals
We had to make 3 big goals we would like to complete, and optionally provide stretch goals.  My goals are:
  1. Migrate data from Google Sheets API to SQL Server
  2. Deploy the project to Amazon Web Services (AWS)
  3. Build out user authentication

Stretch goals are:
  - Build a user account page that shows an overview of the player's characters using the swgoh.gg API.
  - Build a reverse counter list for registered users
  - Build an event tracker that lets a registered user select an event and the characters to track, which would show the current levels and the recommended levels (possibly recommending teams based on the User's roster), and allow users to mark events as completed.  (Uh, oh is that a TO-DO LIST???)
  - Build a squad list function where a registered user could make squad lists for different game modes, maybe with an option to show power levels like 
  - Build in estimated calculations to complete a character based on their gear needs and character shard availability rates.
  - Implement a Required Characters indicator and Required Zetas indicator in the squad builder

### Gameplan
After doing research on AWS's services, I've chosen to use Amazon S3 and Amazon CloudFront to host and deploy the Front End, AWS Lambda to deploy the API, and Amazon RDS hold my SQL Server data.

I've created an ERD for the database structure.  For goals 1 and 2, decided that I'm going to build a local version of the SQL Server first, then the API, then make a development build of the front end to make sure it all works as planned.  Once that's all done, I'm going to deploy each piece, using the same order, so that testing will be straightforward.

Goal 3 _should_ be simple, since we've done Firebase Authentication in class.  I didn't personally do it in our C#/.Net group project, but I do have references to work from.

For my future reference, I'll try to detail what I've done in the next section.
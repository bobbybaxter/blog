--- 
published: true
title: SQL Server Data Import
layout: post
category: [programming, Nashville Software School, SWGOH Counters]
tags: 
- programming
- Nashville Software School
- SWGOH Counters
- SQL Server
---

Importing data into SQL Server Management Studio from Google Sheets took longer than expected.  After an arduous process, here are the steps I had to take:
  - Save the file as a .tsv (tab separated file).  _I couldn't use a .csv (comma separated file) since my data has commas in it._
  - Create the needed tables
  - Remove the Foreign Key constraints on the tables (this was an issue I couldn't get around during import)
  - Right click the **Table** -> **Tasks** -> **Import Data**
  - Choose the Data Source: **Flat File Source**
  - Browse to select the .tsv file.
  - Select **Advanced** on the left menu and change the data type of every `string` to `text stream` for items that should be `nvarchar` or `boolean` for every `bit`, to avoid a truncation error later.
  - Select **Next**
  - Choose the Destination: **SQL Server Native Client 11.0**
  - Change the destination [dbo] to the table you want to import to
  - Select **Edit Mappings** and make sure the **Source** variables map to the correct **Destination** variables
  - Select **Ok** -> **Next** -> **Next**
  - Make sure **Run immediately** is selected
  - Select **Next** -> **Finish** (if all goes well, there won't be any errors and you can close the menu)
  - Once all of the data is imported, add the Foreign Key constraints to the tables
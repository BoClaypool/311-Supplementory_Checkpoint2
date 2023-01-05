# 311-Supplementory_Checkpoint2

Purpose

Supplementory is an inventory app for health supplement users to keep a precise inventory of their supply of health supplements, track costs based on daily/monthly/annual spend and to discover alternative supplement options. 

Data Needs

This app presently uses the standard NextAuth models which include User, Account and Session tables. This may be later changed if NextJS is switched as the framework though whatever is later used will likely be similar.  

Since all supplements legally sold in the US are part of the NIH's DLSD (Dietary Supplement Label Database) which is freely available online, the supplements table will live separate and from the other tables. When a user adds a supplement to their account, the supplement table will have a userID added to it (taken from the user's session information) rather than the other way around. This relates to the goals for the site at scale to provide for adminisrative data insight driven more by which supplements have users rather than the opposite, though of course the opposite can be queried as well.  The supplements table does not yet reflect the future values like UPC, ingredients, type (capsule, powder, caplet, etc) but will soon once the JSON data from the DLSD has been successfully incorporated into meilisearch (almost there). 

The included ERD is reflective of the above.  Presently SQLite is being used with the Sequelize ORM.   
# Overview


In this project, we built new supporting data structures for Udiddit, a fictious social media news agregator site. The existing schema allowed posts to be created by registered users on certain topics, including URL or text content. It also
allows registered users to cast an upvote(like) or downvote(dislike) for any post created on the forum and add comments on
posts. However, the schema only consisted of two denormalized tables with no foreign keys to referential integrity between tables and no constraints to: prevent data duplication, perform data validation prior to inserting new data, enforce uniqueness, or perform checks. It also lacked indexing to speed up queries, a vital addition when working with massive datasets.

After investigating the existing schema using psql and reviewing the features and specifications required by Udiddit to support it's website and administrative interface, we then created a new normalized schema consisting of five tables (a separate table for each entity) with the appropriate constraints to enforce consistency, uniqueness and that only valid data is added to the schema. We also added constraints to handle cases where referenced data gets deleted and indexing to speed up query execution.

Finally, after creating the new schema structure, we migrated the data from the old denormalized schema to the new normalized schema. 

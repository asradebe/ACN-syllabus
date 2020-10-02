---
_db_id: 256
available_flavours:
- python
content_type: project
prerequisites:
  hard:
  - topics/python-specific/mongodb/
  soft: []
ready: true
submission_type: repo
tags: []
title: Python and MongoDB
---

Create a docker composition which will run mongodb. You will be connecting to this container while developing. Be sure to commit your composition to your repo.

Also: DO NOT hardcode your connection configuration into your Python code. Use environmental valiables. Eg: `MONGO_HOST = os.getenv("MONGO_HOST","localhost")`. Make sure you understand why this is a good idea.

## Instructions

You are required to create a back-end service that will help capture basic information about prospective students who come to inquire here at Umuzi.

### database setup

1. Create a database and name it UmuziProspects
2. Create a collection inside the database and name it Visiter.
3. The collection must contain the following fields :

- id: This should be automatically generated by MongoDB
- visitor name
- visitor's age
- date of visit
- time of visit
- name of the person who assisted the visitor
- comments

## functionality

Create a single index script with the following functions:

- `create_visitor`. This should save the Visitor into the database
- `list_visitors` This should return an array of all the visitor names and ids
- `delete_visitor`
- `update_visitor`
- `visitor_details`: given a visitor's id, return all information about that visitor
- `delete_all`

## NOTE

You will be expected to properly test your code. You can use whatever testing framework you want.

## Resources

- https://realpython.com/introduction-to-mongodb-and-python/
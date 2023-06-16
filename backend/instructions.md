#### Backend Focused Challenge

This exercise is to implement the best possible solution to one of the exercises below in the time alloted. We're evaluating your ability to take a set of requirements and create a holistic solution that demonstrates craftsmanship, thoughtfulness and good architectural design. These challenges are **not** a test of how well you know Javascript/Node/Python/SQL etc., nor should you try to impress us with clever or obtuse solutions. If you want to impress us, build something that is beautiful, intuitive and easy to debug/test/extend!

Ideally your solution would have some way to run locally and test the results so we can fully analyze your efforts. However if it's easy enough to deploy to github pages, vercel or any other [free] hosting platform, please do and include the deployment as part of your solution. *We want to learn from you too!*

#### Challenge Part A - Database schema 

##### User Story: As a developer I want to build a highly normalized database schema for storing data

Create a schema for storing the compensation data provided in one of the [available data sets](/data). This schema should be in at least [3NF](https://en.wikipedia.org/wiki/Third_normal_form) with tables for **movies**, **credits**, and anything else that makes sense for the data given.

You ***do not*** have to use the entire dataset to satisfy this challenge.

##### Requirements
* Create a quick database schema diagram
  * Diagram can be programmatically generated or hand drawn
* Upload the dataset to the matching schema
* Perform the following queries. You can export the results of these queries via CSV or attach screenshots of the the output
  * Identify the **top 3** most popular by these 2 production companies: `Walt Disney Pictures` and `Marvel Studios`
  * Identify the **top 5** most expensive `Science Fiction` movies between 2000 and 2023

*A few quick notes on submitting Exercise A*

* Ideally this exercise would use SQLite or Postgres, but any SQL database is OK
* Feel free to upload the entire SQL dump (with schema) of the populated database, or create a script that creates the schema and populates the database with one or more of the provided salary data CSVs. Please do whatever makes the most sense given the time alloted.
* If you'd like to use a scripting language like Python or Ruby along with an ORM (we love [prisma.io](primsa.io)) to make this easier, thats fine with us!

#### Challenge Part B - Basic CRUD functionality 

The goal of this exercise is to design a read-only API (REST or GraphQL API) that returns one or more records from static set of compensation data.

##### User Story: As a developer I want to build a micro service that performs the following functions

* `GET` request - list all movies that return a minium of the following:
    * ID or UUID
    * Movie Title
    * Overview
    * Genres
    * Budget
* `GET` request - fetch a single movie record 
  * **Stretch Goal**: Filter by one or more fields/attributes (e.g. `/movie?fields=title,genre,production-company`)
* `CREATE` request - Create a movie with title as a required parameter 
* `PATCH` request - Update a movie record with any information contained inside a body (JSON formatted)
* `DELETE` request - Delete a movie by it's ID or UUID

*A few quick notes on submitting Exercise B*

* Don't worry about any web application concerns other than serializing JSON and returning via a the above requests.
* The example above (`/movie?fields=title`...) is not set it in stone. Feel free to design the URL structure and JSON schema that you believe creates the best client/consumer experience.

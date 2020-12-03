# Photo Gallery/Carousel

## About The Project

> A recreation of the Trulia listing photo gallery/carousel Component.
1. Visit http://54.219.143.193:3001/ to take a look at the individual component!
1. Visit http://54.177.124.31:3000/ to take a look at the whole listing page with its related projects!

## Table of Contents

* [About The Project](#about-the-project)
* [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
  * [CRUD Operations](#CRUD)
  * [PostgreSQL Setup](#PostgreSQL)
  * [Cassandra Setup](#Cassandra)

## Getting Started

### Prerequisites
* npm

### Installation
1. Clone repo
```sh
git clone https://github.com/HRR49HouseStark/Photos.git
```

2. Install Packages
```sh
npm install
```
### CRUD
3. CRUD Operations

| Type    | Endpoint           | Action            |
| ------- |--------------------| ------------------|
| POST    | '/api/addListing'  | Adds listing      |
| GET     | '/api/listings/:id'| Retrieves listing |
| PUT     | '/api/listings/:id'| Updates listing   |
| DELETE  | '/api/listings/:id'| Deletes listing   |

4. PostgreSQL Setup
    - Install homebrew if on Mac OS (other OS you have to find out how to install it on your own)
    - To install postgres, run: $ brew install postgres
    - To start postgres run the command: $ brew services start postgresql
    - To access the shell, run: $ psql postgres
    - Create a database by typing: 'createdb <database>'
    - I would suggest you use 'SDC' for your database unless you want to manually change the schema.sql file
    - To create the tables in your database, type the following in the postgres shell: '\i schema.sql'
    - To see all relations in the database, type: \dt
    - While using the SDC database (\c SDC), type the following to see the table: SELECT * FROM listings
    - Great! Now your database is set up with your table and all you need to do is populate it.
    - reference: https://gist.github.com/ibraheem4/ce5ccd3e4d7a65589ce84f2a3b7c23a3

5. Cassandra Setup
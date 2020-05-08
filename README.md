# Lyrics-Search-Engine

This was a project submitted for a class assignment for my Database Systems course.

## Overview

In this project, I designed a very simple search engine that allows users to search and rank songs according to specific keywords. 

This project used several technologies, but I was only tasked with working with PostgreSQL and Python. The following technologies were used in the project, but not touched by me.
* Nginx: a high performance HTTP/web server
* Flask: a popular micro-platform for web and API development
* uWSGI​: a protocol and serves as a "glue" between Nginx and Flask
* Jinja2​: ​is a templating engine used by Flask to write standard HTML files with embedded special tokens

The files that I were responsible for were the following:
* search.py
* searchengine.py
* load.sql
* schema.sql
* index.html
* results.html

## My tasks
1. Database Setup
	- Wrote queries to create database tables with the correct data types, keys, and constraints
	- Loaded the data (60K+ songs and their information) into these tables
	
2. Search Ranking Query
	- Wrote a SQL query that computed the TF-IDF score for each token in each song
	- Handled both the AND case and the OR case
	- Summed across the TF-IDF scores to determine how well a song matched a query
	
3. Connect + Disconnect from Database
	- Wrote Python code to connect to the PostgreSQL instance running on a VM 
	- Closed connection whenever a failure occurred
	
4. Integrate database query in search( ) function
	- I wrote SQL queries to handle the user's input and extract results from the database
	- Each result lists the name of the song and the artist
	
5. Protection from SQL Injections
	- Used prepared statements to format user input such that SQL injections aren't possible

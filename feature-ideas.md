---
title: Feature Ideas
description: Ideas for features that aren't in our roadmap yet.
published: true
date: 2021-05-06T18:19:16.652Z
tags: 
editor: markdown
dateCreated: 2021-04-20T19:47:31.098Z
---

These are potential feature ideas for Mathesar. Each section represents a conceptual grouping of features.

> Please note that this list is long and disorganized. Some are slated to be built in our roadmap, and others we might not build at all.
{.is-warning}

## CRUD For Tables & Schemas
Users should be able to perform these actions in both the GUI and API:

### GUI & API
- Create a new table
	- in an existing schema
	- in a new schema
- Create a table via importing data via
	- CSV
	- TSV
- View a table and see what type each column is.
- Edit a table name
- Edit a schema name
- Delete a table
- Delete a schema

### GUI only
- Create a table via
	- copy/paste from a spreadsheet
- Edit the data in their table using a spreadsheet-like interface
	- e.g. fill down cells by dragging a corner

## Filtering, Sorting, Grouping
Users should be able to perform these actions in both the GUI and API:
- Filter the table by rules applied to data in various fields.
- Sort the table by various fields.
- Group results by the first character of any given field.
- Group results by the first word of any given field.
- Apply multiple filters, groups, and/or sorts at once.

## Multiple Types Support
Users should be able to perform these actions in both the GUI and API:
- Change the type of data per-column to any type supported by Postgres or PostGIS
	- The data in the column will be validated.
- Import data via any supported import method and have the types of data automatically detected during the import process
	- Types are suggestions and can be changed by the user.

## Boolean Type
- Add new type (use Postgres type if possible):
	- Boolean
- Autodetect this type during import
- Allow user to change columns to this type
- Add additional grouping options by value (yes/no)

## New Text Types
- Add new types:
	- Email
	- URL
- Autodetect these types during import
- Allow user to change columns to these types
- Add additional grouping options:
	- Email: Domain
	- URL: TLD, Protocol

## Numeric Types
- Add new types, using existing Postgres types where possible:
	- Money (with specified currency)
	- Percentage
	- Number
- Autodetect these types during import
- Allow user to change columns to these types
- Add additional grouping options:
	- Number: Range (calculate range options dynamically based on data, e.g. if data varies from 1-100, ranges could be 1-10, 10-20, etc.)
	- Money: Range, Currency
	- Percentage: Range
  
## Date and Time Types
- Add new types, using existing Postgres types where possible:
	- Date & Time
	- Date
	- Time
	- Duration
- Autodetect these types during import
- Allow user to change columns to these types
- Add additional grouping options:
	- Date & Time, Date, Time support all grouping options supported by Postgres EXTRACT function.
	- Duration: Range
- Allow filtering using natural language for dates (e.g. "next month")

## Relationship Type
Users should be able to:
- Create a column that represents a relationship to another record (e.g. Book --> Author)
- "Extract" a column from a table into a separate table (change the underlying schemas)
- Choose which field from the other table to use to represent the relationship (e.g. if I'm displaying the Author in the Book table, I want to see the Author's name, not ID)

## Views
Users should be able to:
- Save filtered/sorted/grouped tables as views.
- Create a calendar view based on date and time fields in their data
- Create a histogram chart view based on their data
- Create a pie chart view based on their data
- Create a line graph view based on their data
- Create a scatter plot view based on their data
- View all saved views and switch between views
- Set a default view for a table/schema
- Delete a view
- Rename a view

## Computed Data
Users should be able to:
- Create a new column that computes data from other columns using forumulas.
- Create "subtotals" for grouped views
	- Support different types of subtotals: SUM, AVG, MIN, MAX, MED
- Create summary views based on subtotals, and use that data in views
	- e.g. given a database of sales with dates, create a summary view of sales per quarter and put that into a histogram


## Installation and Configuration
Users should be able to:
- Follow provided instructions to install Mathesar on a server.
	- The installation process should only install PostgreSQL if needed.
- Access existing PostgreSQL databases via Mathesar using existing PostgreSQL user credentials.
	- Existing databases should reflect all columns and types correctly in the user interface.
- Set up a PostgreSQL server automatically if none exists.
- Create a new database from scratch.
- Create an initial user if needed.
- Configure sending email (for password resets, notifications)

## User Management
Users should be able to:
- Log in
- Log out
- Create a new user with permissions: admin, editor, viewer
- Change a user's permissions
- Reset a user's password
- Reset their own password (if email is enabled)

## Collaboration
- Users should be able to share tables, schemas, and/or views with either:
	- the general public (no sign in required)
	- all signed in users
	- specific users
- Each of these should support:
	- admin, view, edit permissions
- Existing postgres permissions should be respected/reflected

## Data Workflow Improvements
Users should be able to:
- Search for data across various tables and schemas
- Bulk edit data
- Bulk import new data into an existing collection
- Export data to:
	- SQL
	- CSV
	- TSV
	- JSON
	- Excel
	- XML



## Additional Imports
Users should be able to import data in the following additional formats:
- SQL
- JSON
- XML
- Google Sheets import (via API)
- Excel file upload
- Excel web import (via API)
- Apple Numbers file upload
- Collabora import
- Airtable

## Location Type
- Add new type, using existing PostGIS type where possible:
	- Location
- Autodetect this type during import
- Allow user to change columns to this type
- Add additional grouping options:
	 Street Address
	 Country
	 Administrative Area Level 1 *(in the US, these are states)*
	 Administrative Area Level 2 *(in the US, these are counties)*
	 Administrative Area Level 3
	 Administrative Area Level 4
	 Administrative Area Level 5
	 Locality *(city/town)*
	 Sublocality *(subdivision of city/town)*
	 Neighborhood
	 Postal Code
	 Latitude
	 Longitude

The attributes of the location column type are based on results returned by the [Google Maps Geocoding API](https://developers.google.com/maps/documentation/geocoding/overview), Since they\'ve done the work of putting addresses into a global format.

## Phone Number Type
- Add new type
	- Phone Number
- Autodetect this type during import
- Allow user to change columns to this type
- Add grouping options:
	- Country Code
	- Area Code

## Additional Fields
- File field (for images, attachments, etc.)
- IP Address field
- Formula field (use of spreadsheet like formulas)
- JSON field

## Additional Views
- Map view
- Card (Gallery) view
- Kanban view
- Data modeling view (of entire schema or database)

## Forms
- Create forms that allow users to enter data into views

## Data Syncing
Users should be able to sync data both ways from:
- Google Sheets
- Airtable
- Excel (web)
- Airbyte connectors?

## Data Suggestions
Users should get suggestions about:
- Visualizations they can apply to their data
- Aggregations they can apply to their data
- Schema imporovements they can make to their data

## Versioning
Users should be able to:
- Save a snapshot of their database, schema, or table.
- Revert to a previous version of their database, schema, or table.
- Undo and redo recent actions.

## Events
Events in the system should be exposed via an API. e.g.
- New table created
- Table schema changed
- New data added

## Notifications
Users should be able to:
- Get email notifications of various events.
- Get web notifications of various events.

## Templates
Users should be able to:
- Save databases, schemas, applications as templates.
- Use a template to create a new database, schema, or application.
- Edit template attributes.
- Delete a template.
- Browse existing templates.
- Search for templates.

## Improved User Management
Users should be able to:
- Create teams of users, teams can have similar permissions to users.

## API
- API key management
- API documentation

## Freeform Data Support
- UI to handle freeform data (JSON) well
- Suggest conversion of non-tabular data to tabular data based on schema
- Automatically generate appropriate tabular data if consistency exists in imported freeform data

## SQL Exploration
- Run SQL from the web interface

## Comments
- Comment on data

# Postgres Audit Triggers JSON

A simple, customisable table audit system for PostgreSQL implemented using
triggers.

This trigger is based on https://github.com/2ndQuadrant/audit-trigger.
It has been modified to include the following features:

  * Customizable "application.name" setting for specifying source application
  * Customizable "application.user" setting for specifying active application user
  * The original and diff columns are now stored in JSONB instead of HSTORE.
    The JSONB diff value is a recursive JSONB diff of changes made to the original
    record and any JSONB columns within.
  * Additional naming convention tweaks
  * Automatic table enrolment by default

Requires PostgreSQL 9.5+

## To use:
Run the contents of [audit.sql](./audit.sql) in a newly set up database.

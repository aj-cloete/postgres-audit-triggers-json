A simple, customisable table audit system for PostgreSQL implemented using
triggers.

This trigger is based on https://github.com/2ndQuadrant/audit-trigger.
It has been modified to include the following features:

  * Customizable "application.name" setting for specifying source application
  * Customizable "application.user" setting for specifying active application user
  * The original and diff columns are now stored in JSON instead of HSTORE.
    The JSON diff value is a recursive JSON diff of changes made to the original
    record and any JSON columns within.
  * Additional naming convention tweaks

Requires PostgreSQL 9.5+

I use these SQL stored procedures for my daily monitoring.

Dailymonitoring: It checks which sql job has ran already or still running on our server.

sp_extract_monitor: This script checks and compares what sql tables have been extracted from AWS (every angle server) to our sql server on a given day. Once all the tables have been extracted for a given job, the sql job starts autoamtically.

sp_mass_extract_monitor: THis script uses the previous sp_extract monitor stored procedure and just loops trough the given criteria specified in the mass stored procedure.

dataArchiving : We use this script to move rows into archive database, so we can improve performance in live tables which are used for tableau and BI dashboards.

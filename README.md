# CSVtoMySQL
PHP script, that is executed from the command line, which accepts a CSV file as input
(see command line directives below) and processes the CSV file. The parsed file data is to be
inserted into a MySQL database. A CSV file is "users.csv".
The PHP script handle the following criteria:
• CSV file contain user data and have three columns: name, surname, email
(see table definition below)
• CSV file have an arbitrary list of users
• Script iterate through the CSV rows and insert each record into a dedicated
MySQL database into the table “users”
• The users database table created/rebuilt as part of the PHP script.
This is defined as a Command Line directive below
• Name and surname field set to be capitalised e.g. from “john” to “John”
before being inserted into DB
• Emails set to be lower case before being inserted into DB
• The script validates the email address before inserting, to make sure that it
is valid (valid means that it is a legal email format, e.g. “xxxx@asdf@asdf” is not
a legal format). In case that an email is invalid, no insert made to
database and an error message reported to STDOUT.

# User Table Definition
The MySQL table should contain at least these fields:
• name
• surname
• email (email should be set to a UNIQUE index).

# Script Command Line Directives
The PHP script include these command line options (directives):
• --file [csv file name] – this is the name of the CSV to be parsed
• --create_table – this cause the MySQL users table to be built (and no further
• action will be taken)
• --dry_run – this used with the --file directive in case we want to run the
script but not insert into the DB. All other functions will be executed, but the
database won't be altered
• -u – MySQL username
• -p – MySQL password
• -h – MySQL host
• --help – output the above list of directives with details.

# Default connection details
user : root
password : blank ( not set )
host : localhost or 127.0.0.1
Your connection details may difer depending of your server configuration. 

# How to change default connection details?
You can edit them in functions.php 

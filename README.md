# PostgreSQL

DBA on 3/14  

Feature:

Postgres is an object-relational database, while MySQL is a purely relational database. This means that Postgres includes features like table (model class) inheritance and function overloading, which can be important to certain applications. Postgres also adheres more closely to SQL standards.

-----------------------------------------------------------------------

| Download & Install

https://postgresapp.com/downloads.html

    $ brew install postgresql

    $ brew services start postgresql
    ==> Successfully started `postgresql` (label: homebrew.mxcl.postgresql)

    $ psql -V
    psql (PostgreSQL) 12.2
    
    $ psql
    
    $ pintred(DB_NAME)=# 
    SELECT setting FROM pg_settings WHERE NAME='data_directory';
         
  
       >>>
         
         
         setting     
         
         
        -------------------------
         /usr/local/var/postgres
        (1 row)



-----------------------------------------------------------------------

    \g or terminate with semicolon to execute query

    \q to quit

    $psql back to psql prompt

    then-> pintred(DB_Name)=#

    \help for sql

Available help:

      ABORT                            CREATE USER
      ALTER AGGREGATE                  CREATE USER MAPPING
      ALTER COLLATION                  CREATE VIEW
      ALTER CONVERSION                 DEALLOCATE
      ALTER DATABASE                   DECLARE
      ALTER DEFAULT PRIVILEGES         DELETE
      ALTER DOMAIN                     DISCARD
      ALTER EVENT TRIGGER              DO
      ALTER EXTENSION                  DROP ACCESS METHOD
      ALTER FOREIGN DATA WRAPPER       DROP AGGREGATE
      ALTER FOREIGN TABLE              DROP CAST
      ALTER FUNCTION                   DROP COLLATION
      ALTER GROUP                      DROP CONVERSION
      ALTER INDEX                      DROP DATABASE
      ALTER LANGUAGE                   DROP DOMAIN
      ALTER LARGE OBJECT               DROP EVENT TRIGGER
      ALTER MATERIALIZED VIEW          DROP EXTENSION
      ALTER OPERATOR                   DROP FOREIGN DATA WRAPPER
      ALTER OPERATOR CLASS             DROP FOREIGN TABLE
      ALTER OPERATOR FAMILY            DROP FUNCTION
      ALTER POLICY                     DROP GROUP
      ALTER PROCEDURE                  DROP INDEX
      ALTER PUBLICATION                DROP LANGUAGE
      ALTER ROLE                       DROP MATERIALIZED VIEW
      ALTER ROUTINE                    DROP OPERATOR
    :

or 

\? for psql cli

    General
      \copyright             show PostgreSQL usage and distribution terms
      \crosstabview [COLUMNS] execute query and display results in crosstab
      \errverbose            show most recent error message at maximum verbosity
      \g [FILE] or ;         execute query (and send results to file or |pipe)
      \gdesc                 describe result of query, without executing it
      \gexec                 execute query, then execute each value in its result
      \gset [PREFIX]         execute query and store results in psql variables
      \gx [FILE]             as \g, but forces expanded output mode
      \q                     quit psql
      \watch [SEC]           execute query every SEC seconds

    Help
      \? [commands]          show help on backslash commands
      \? options             show help on psql command-line options
      \? variables           show help on special variables
      \h [NAME]              help on syntax of SQL commands, * for all commands

    Query Buffer
      \e [FILE] [LINE]       edit the query buffer (or file) with external editor
      \ef [FUNCNAME [LINE]]  edit function definition with external editor
      \ev [VIEWNAME [LINE]]  edit view definition with external editor
      \p                     show the contents of the query buffer
      \r                     reset (clear) the query buffer
      \s [FILE]              display history or save it to file
      \w FILE                write query buffer to file

-----------------------------------------------------------------------
General options:

    -c, --command=COMMAND    run only single command (SQL or internal) and exit

    -d, --dbname=DBNAME      database name to connect to (default: "pintred")

    -f, --file=FILENAME      execute commands from file, then exit

    -l, --list               list available databases, then exit

    -v, --set=, --variable=NAME=VALUE

                           set psql variable NAME to VALUE
                           
                           (e.g., -v ON_ERROR_STOP=1)
                           
      -V, --version            output version information, then exit

      -X, --no-psqlrc          do not read startup file (~/.psqlrc)

      -1 ("one"), --single-transaction

                           execute as a single transaction (if non-interactive)
                           
      -?, --help[=options]     show this help, then exit

      --help=commands      list backslash commands, then exit
      
      --help=variables     list special variables, then exit

Input and output options:

      -a, --echo-all           echo all input from script

      -b, --echo-errors        echo failed commands

      -e, --echo-queries       echo commands sent to server

      -E, --echo-hidden        display queries that internal commands generate

      -L, --log-file=FILENAME  send session log to file

      -n, --no-readline        disable enhanced command line editing (readline)

      -o, --output=FILENAME    send query results to file (or |pipe)

      -q, --quiet              run quietly (no messages, only query output)

      -s, --single-step        single-step mode (confirm each query)

      -S, --single-line        single-line mode (end of line terminates SQL command)


Output format options:

      -A, --no-align           unaligned table output mode

          --csv                CSV (Comma-Separated Values) table output mode

      -F, --field-separator=STRING
                               field separator for unaligned output (default: "|")
      -H, --html               HTML table output mode

      -P, --pset=VAR[=ARG]     set printing option VAR to ARG (see \pset command)

      -R, --record-separator=STRING
                               record separator for unaligned output (default: newline)

      -t, --tuples-only        print rows only

      -T, --table-attr=TEXT    set HTML table tag attributes (e.g., width, border)

      -x, --expanded           turn on expanded table output

      -z, --field-separator-zero
                               set field separator for unaligned output to zero byte

      -0, --record-separator-zero
                               set record separator for unaligned output to zero byte

Connection options:

      -h, --host=HOSTNAME      database server host or socket directory (default: "local socket")

      -p, --port=PORT          database server port (default: "5432")

      -U, --username=USERNAME  database user name (default: "pintred")

      -w, --no-password        never prompt for password

      -W, --password           force password prompt (should happen automatically)

For more information, type "\?" (for internal commands) or "\help" (for SQL
commands) from within psql, or consult the psql section in the PostgreSQL
documentation.

Report bugs to <pgsql-bugs@lists.postgresql.org>.



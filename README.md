teradataR
=========

R package to perform in-database analytics using Teradata database.

Should be compatible with both R version 2 and 3.

## Dependencies

+ RJDBC
 + rJava
+ RODBC?

## Installation

To install the package, issue the following commands from R:

    install.packages("devtools")
    library("devtools")
    install_github('KarolTx/teradataR)

## Usage on Linux

* download Teradata JDBC driver
* insert following lines before making a connection

    .jinit()
    &#35; path of JDBC driver:
    path.jdbcdriver <- "/path/to/jars"
    class.jdbcdriver <- paste0(path.jdbcdriver, c("terajdbc4.jar", "tdgssconfig.jar"), collapse = ";")
    &#35; for this to work on a unix-like OS, class path needs to be added:
    .jclassPath()  &#35; check class path
    .jaddClassPath(paste0(path.jdbcdriver, "terajdbc4.jar"))
    .jaddClassPath(paste0(path.jdbcdriver, "tdgssconfig.jar"))

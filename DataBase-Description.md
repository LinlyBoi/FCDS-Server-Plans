# Phases in building the hardware database:

    Describing the database that is to be built over the course of 

    days.
    Modelling the database in an Entity-Relationship diagram.
    Developing the skeleton of the database in Postgresql.
    Collecting and Inserting the data into their respective tables.

# 1) Description

The task to put all of the faculty's hardware into a digital database that will be hosted on the server cluster that has been set up should be described prior to taking any further steps.

The known hardware that will be put into the database:

    Desktop PCs
    Monitors
    Laptops
    Printers
    Photocopiers

Bringing the total amount of tables thus far up to 5 tables.

For the Desktops' table it will have the following attributes:

    Serial Number.
    Hostname.
    Room where it is put.
    Status. (Stored, In Use, Under Maintenance)

For Monitors' table it will have the following attributes:

    Serial Number.
    Desktop to which it is connected to.
    Room where it is put.
    Status. (Stored, In Use, Under Maintenance)

For Laptops' table it will have the following attributes:

    Serial Number.
    Hostname.
    Room where it is put.
    Status. (Stored, In Use, Under Maintenance)

For Printers' table it will have the following attributes:

    Serial Number.
    Room where it is put.
    Status. (Stored, In Use, Under Maintenance)

For Photocopiers' table it will have the following attributes:

    Serial Number.
    Hostname.
    Room where it is put.
    Status. (Stored, In Use, Under Maintenance)


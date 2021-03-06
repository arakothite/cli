CIC Command Line Interface  [![Build Status](https://travis-ci.org/InteractiveIntelligence/cli.svg)](https://travis-ci.org/InteractiveIntelligence/cli)
=======
The CIC Command line interface tool will allow you to interact with CIC through the command line.  

Usage: cic < command > [< args >]

Available commands:

    help      Show this help
    defaults  Show the default values for a new item of the configuration type
    delete    Perform a delete on a particular configuration item
    features  Gets feature information about the cic server
    get       Gets a configuration object
    interaction  Performs the action on an interaction
    login     Log in to a CIC server
    logout    Log out from CIC
    makecall  Places a call to the target for the currently logged in user
    select    Perform a query on a particular configuration type
    status    Get or sets a user's status
    version   Gets version information about the cic server
    whoami    Show information about currently logged in user

Run 'cic help [command]' for details.


Examples
========

Find Current User's Extension
-----------------------------

    cic login http://morbo:8018 kevin.glinski 1234
    cic whoami | grep extension


Get All User's and Their Extensions and Save to a File
------------------------------------------------------
    cic login http://morbo:8018 kevin.glinski 1234
    cic select extension, workgroups from user > output.txt

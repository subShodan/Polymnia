This is Project Polymnia
==========================

## Development Design Methodology .
    
    The design methodology essentially derives from concurrent systems that monitor different aspects of the App ecosystem.
    These concurrent systems are individualized as *Modules*.

    Modules operate on parallel files and should not interact with same files. An obvious distinction between files should be established and respected throughout the duration of development.


Feature List
------------
Discussions pending


Modules 
-------

## Athena Module:
   
    This module takes care of the styling for the web app. Based on TailswindsCSS, The classes are abstracted to utility based representations.

#### Bringing it online:
  
    npx tailwindcss -i ./resources/css/input.css -o ./resources/css/app.css --watch

#### Configuration Files:

    - /resources/input.css
    - tailwind.config.js

------------------------------------------------------
##  Janus Module 
    
    This is an extended iteration of Adonis's very own authentication system. Janus can be visualized as a two-faced entity with Admin and User authentication subroutines. This also takes care of the transaction cookies and abstracts them to configuration rather than code.

    It is invoked autonomously.

#### Configuration Files:
    TBD
-----------------------------------------------------
## Coeus Module

    This module covers all the global database transaction implementations. Its submodule HYPNUS is the direct wrapper around LUCID ORM. 

#### Configuration Files:
    TBD
-------------------------------------------------------

## Hypnus Module

    A wrapper around Lucid. Affects all the Models and DB migrations. Lives on the edge of DB and Typescript Models.  

#### Configuration Files:
    TBD

--------------------------------------------------------

## Hermes Module

    Takes care of all the Routing through the app and APIs. Only brings the data to controller. Needs appropriate HTTP verbs to communicate.

#### Configuration Files:
    TBD

-----------------------------------------------------------

## Hephaestus Module

    This enables custom commands in the app ecosystem. Could be used to generate customized templates for frontend or essential scripts for backend.

#### Bringing it online:
  
    node ace <subroutine>

#### Configuration Files:
    TBD

------------------------------------------------------------

## Cronus Module

    All the daemons that need to run for app performance measurement.
    Generally placed at the bottom most tier and should not be overwritten by subsequent processes. Should only be used for monitoring. 

#### Configuration Files:
    TBD
-------------------------------------------------------------

## Thanatos Module

    Ensures proper error/exception handling for graceful death of App.

#### Configuration Files:
    TBD

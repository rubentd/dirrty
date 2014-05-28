dirrty
===========

jquery plugin to detect if the fields of a form had been modified 
If a field has been modified then the form is dirrty

- Detect the moment when the form gets dirty, and trigger a custom event, for example enable a "save changes" button
- Detect the moment when the form gets clean again, and trigger a custom event, for example disable the "save changes" button, cause is not necesary
- Promt the user to save changes before leaving if the form is dirty

The name comes from Christina Aguilera's 2002 song:
https://www.youtube.com/watch?v=2xMWrKhLJq4


Usage
--------

$("#form-id").dirrty();


Options
--------

*preventLeaving* true | false
*leavingMessage*  Message to show when user tries to leave with a dirty form
*onDirty* Function to be triggered when the form gets dirty
*onClean* Function to be triggered when the form gets clean again

Methods
---------

$("#form-id").dirrty("isDirty");

Lets you know if the form is dirty at a givent moment
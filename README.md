dirrty
===========

lightweight jquery plugin to detect if the fields of a form had been modified.   
If a field has been modified then the form is dirrty  

- Detect the moment when the form gets dirty, and trigger a custom event, for example enable a "save changes" button
- Detect the moment when the form gets clean again, and trigger a custom event, for example disable the "save changes" button, cause is not necesary
- Prompt the user to save changes before leaving if the form is dirty

The name comes from Christina Aguilera's 2002 song:
https://www.youtube.com/watch?v=2xMWrKhLJq4


Usage
--------
```javascript
// this can be called on individual forms by id or on "form" to target all forms
// simultaneously
$('#form-id').dirrty({
  preventLeaving: false

  // this function is called when the form.trigger's "dirty"
}).on("dirty", function() {
  console.log("I'm dirty!")

  // this function is called when the form.trigger's "clean"
}).on("clean", function() {
  console.log("I'm clean!")
});
```

Options
--------
| name | description | default |
|---|---|---|
| preventLeaving | show a message when a user attempts to leave the page with a dirty form | true
| leavingMessage | the message to show when a user tries leaving the page with a dirty form. **Most modern browsers [no long support](https://developer.mozilla.org/en-US/docs/Web/API/WindowEventHandlers/onbeforeunload#Browser_compatibility) setting a custom message and will show their own message regardless.** | "You have unsaved changes"
| onDirty | **depricated** - [see change](https://github.com/sdomino/dirrty/commit/ad9f0d3bf5cb958ac9a309741815bf9f69444325) | function(){} |
| onClean | **depricated** - [see change](https://github.com/sdomino/dirrty/commit/ad9f0d3bf5cb958ac9a309741815bf9f69444325) | function(){} |  

Methods
---------

`$("#form-id").dirrty("isDirty");`

Lets you know if the form is dirty at a givent moment

[Live Demo](http://rubentd.com/dirrty)

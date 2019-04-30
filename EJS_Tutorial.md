# EJS tutorial

#### Documentation can be found here: https://ejs.co/ and here: http://harpjs.com/docs/development/ejs

First make sure the file extension of the HTML file is *.ejs, not .html. 
This won't change your preexisting html, but will allow the use of new features.  

## Adding partials

A 'partial' is just a section of a full HTML document. For example the navbar and footer and put into
partials so each separate page can  have the same navbar and footer.

Here is the syntax:
```
    <%- partial("partials/[partial name].ejs") %>
```

Replacing the name would look like:
```
    <%- partial("partials/navbar.ejs") %>
```

#### Notes

- The `<%- ->` tells harpjs that inside is EJS code. The `-` means that we don't want to escape
values that are outputted.
- `partial()` is a function call specific to harpjs, and lets us get other EJS/HTML file to plug in.
- `"partials/[partial name].ejs` is relative to the **/public* folder, not the current EJS file.
- partials don't have to be put in */partials*, but it is recommended.

## Data in harpjs

Data has to be put in a *_data.json* file, of course in any JSON format. It
is flexible and can be used anyway you want like normal JSON. This allows for
automatic content generation. 

Here is an example, given these files both in */public*:

**_data.json**
```
    {
     "hello-world": {
       "title": "Hello World.",
       "date": "2019-02-28"
     },
     "hello-brazil": {
       "title": "Hello Brazil.",
       "date": "2019-03-04"
     }
   }
``` 

**example.ejs**
```
        <% for (var article in public._data) { %> 
            <h2><%= public._data[article].title %></h2>
            <p><%= public._data[article].date %></p>
        <% } %>
```

Will output:
```
            <h2>Hello World.</h2>
            <p>2019-02-28</p>
        
            <h2>Hello Brazil.</h2>
            <p>2019-03-04</p>
```

#### Notes

- The data file is placed in the *public.[folder path]._data* variable, were folder path is the 
location from */public*.
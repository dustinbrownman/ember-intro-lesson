* Download ember starter kit
* briefly describe some of what's there
* download ember inspector
* delete stuff and start as fresh as possible
* start with Router
* define Route
* write model method
* define 'post' model - talk about data store and fixtures (FixtureAdapter)
* write setupController method
* write 'PostsController'
* write renderTemplate method
* ...

Today, we're going to get started with Ember.js, a Client-side MVC [NEED: some description of what ember is and what some of the advantages are...].

Let's start by downloading the starter kit from [Emberjs.com](http://emberjs.com). Unzip the file then move `starter-kit-1.5.1` to the `Code` folder and rename it `ember-blog`. Open up the project in Sublime Text and let's explore some of the different components.

First, open `index.html`. At first glance, this looks pretty familiar. It's really just a standard `HTML` page. In the `<head>` you'll notice some the title and some stylesheets being being loaded. Things start to get strange inside the `<body>`. At the top. you should see something like this:

<div class="filename">index.html</div>
```
<script type="text/x-handlebars">
  <h2>Welcome to Ember.js</h2>

  {{outlet}}
</script>
```
This is called a __template__. We won't worry too much about these right now, but know templates are written in __Handlebars__, which gets its name from the curly braces it uses to denote logic (supposedly, they look like a sideways handlebar mustache). Handlebars is similar to ERB, but instead of using Ruby to write our logic, it uses its own special syntax.

Now look at the scripts being loaded at the bottom of the `<body>`.

```
<script src="js/libs/jquery-1.10.2.js"></script>
<script src="js/libs/handlebars-1.1.2.js"></script>
<script src="js/libs/ember-1.5.1.js"></script>
<script src="js/app.js"></script>
```

Here we are loading Ember and its dependences (jQuery and Handlebars) on to the page. The last line is loading `app.js`, where we'll define and initialize our Ember application. Any other files we add to our app will need to be included below so everything is compiled in the right order. [NEED: revisit this wording. may not be quite right]

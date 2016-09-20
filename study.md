# Rails as an API Study

Use your favorite search engine and the provided readings to research and answer
the following questions (no prior knowledge is expected).

In your answers, be sure to cite any relevant sources you consulted in your
search. We ask you to write answers in your own words in order to see how you
process what you've read. Please do not answer with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

Please note:

-   Many of the readings will mention the "view" layer. We won't be covering the
    view layer in this program.
-   We'll use our [rails-api-template](https://github.com/ga-wdi-boston/rails-api-template)
    repository as the basis for our rails applications.
    This template excludes the "view" layer.

## Required Readings

-   [Starting Ruby on Rails: What I Wish I Knew | BetterExplained](http://betterexplained.com/articles/starting-ruby-on-rails-what-i-wish-i-knew/)
-   [Intermediate Rails: Understanding Models, Views and Controllers | BetterExplained](http://betterexplained.com/articles/intermediate-rails-understanding-models-views-and-controllers/)
-   [Getting Started with Rails — Ruby on Rails Guides](http://guides.rubyonrails.org/getting_started.html)
-   [The Rails Command Line — Ruby on Rails Guides](http://guides.rubyonrails.org/command_line.html)
-   [Rails Routing from the Outside In — Ruby on Rails Guides](http://guides.rubyonrails.org/routing.html)
-   [Action Controller Overview — Ruby on Rails Guides](http://guides.rubyonrails.org/action_controller_overview.html)

## Define Model Responsiblities

In your own words, define what the responsibilities of the model layer are in
Rails.

```md
The model layer does most of the grunt work in Rails. It holds Ruby classes that
talk to the database, performs logic, and holds and stores data.
```

## Define Controller Responsiblities

In your own words, define what the responsibilities of the controller layer are
in Rails.

```md
The controller layer acts almost like a gatekeeper. It receives user requests/inputs
(i.e. a URL, data submission) and decides what do to with them. Ideally, controllers
should say lean and only take inputs, call model methods and pass outputs to the view.
If you find that your controller has business logic in it, refactor it to the model.
```

## Define Router Responsiblities

In your own words, define what the router does in Rails.

```md
In order for the controller to do its job, the router has to help it out. The router
decides which controller receives which requests. Many times there will be more than
one route to each controller and different routes can be served by different actions.

```

## The Request-Response Cycle in Rails

Starting with a client making a GET request to a particular URL, describe how
the parts of Rails interact to produce and send a response.

```md
1. Browser makes a request for a URL such as http://www.facebook.com/photo/20.
2. The web server receives the request and uses routes to decide which controller to use.
3. Once server will then use a dispatcher to create a new controller to make the GET request and pass the parameters.
4. The controller receives the GET request and pings the model to retreive photo 20.
5. Model retreives photo 20 for the controller.
6. Then the controller gives photo 20 to the view to generate the HTML.
7. Once the controller receives the data from both the model and view it'll return everything to the server.
8. The server then takes turns the raw data into an HTTP response and sends it to the user.
```

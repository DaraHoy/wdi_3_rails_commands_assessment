# Rails Commands Quiz

Fork, clone, and write your answers directly in this file. Then submit a pull request.

### Question 1

I want to start a new Rails project/app called `BunnyApp`. What command should I type in the terminal?

$ rails new BunnyApp -d postgresql (if using PG)

### Question 2

I want to create a new model called `Bunny`, with the following attributes: name (string), color (string), and age (integer). What command(s) should I type in the terminal and/or Sublime? (In your answer, create both a migration and the model file.)

$ rails g model Bunny name:string color:string age:integer
$ rails db:migrate

### Question 3 rails

What does the command in Question 2 do, exactly? What files are created, where are they located, and what does the database look like at this time? Explain.

The '$ rails g model <Bunny>...' command uses rails generator to create a model for your database table in this case <Bunny>, it also takes any arguments that follow it and creates columns for that model and assigns to it your selected data type. for example 'name:string' will create a column in table for 'name' and is expecting string type data which is how it will be treated by the logic. At this time, assuming we've ran the migrate command, the data base(db) would have a single table called Bunny with the columns id, name, color, and age.

### Question 4

I want to create a database and make it reflect the new model I created in Question 2. What command(s) should I type in the terminal?

$ rails db:create
$ rails db:migrate

### Question 5

I want to look at the actual database that has been created. What command should I type in the terminal?

$ rails c
Once inside your Ruby command line execute a query command to confirm your Model/Class was created.

For example if we had a Bunny model: Bunny.all => <Bunny table data>, so Bunny.all will return your <Bunny table data>

### Question 6

I want to see a list of all the URLs available in my app, along with the HTTP requests and controllers associated with them. What command should I type in the terminal?

$ rails route => all the URLs availble in your app along with controller info.
Also useful would be to use this URL inside your browser for more info: http://localhost:3000/rails/info/routes


### Question 7

What line should I add to `config/routes.rb` to create a complete set of RESTful routes for a "bunnies" resource?

resource :bunnies

### Question 8

According to standard Rails conventions, what directory and filename would the BunniesController be located in, starting from the root of the project?

.../BunnyApp/app/controllers/bunnies_controller.rb

### Question 9

According to standard Rails conventions, what directory and filename would the "show" view for bunnies be located in, starting from the root of the project?

.../BunnyApp/app/views/bunnies/show.html.erb

### Question 10

I have worked on my app and finally want to see it in action. What command should I type in the terminal, and where should I navigate to in my browser?

$ rails s
This command will enable your webserver then navigating to the following URL in your browser:
http://localhost:3000
This is the standard Ruby server URL

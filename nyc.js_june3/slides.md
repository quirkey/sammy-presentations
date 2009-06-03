!SLIDE

# Sammy.js

!SLIDE

# What is Sammy?

!SLIDE

![Sammy](images/sammy2.jpg)

## Classy.

!SLIDE

![Sinatra](images/sinatra.jpg)

## Kind of like this guy . . .

!SLIDE

![Sinatra](images/sammy1.jpg)

## Classier.

!SLIDE

# The short description

!SLIDE

> Sammy is a tiny JavaScript framework, built on top of jQuery, inspired by Ruby's Sinatra

!SLIDE

# Zuh?

!SLIDE

# Sinatra:

@@@ ruby
# app.rb
class MyApp < Sinatra::Default
  
  get '/user/:name' do
    @user = User.find_by_name(params['name'])
    erb :user
  end
  
  post '/user/' do
    @user = User.create(params['user'])
    redirect "/user/#{user.name}"
  end
  
end
@@@

!SLIDE

# Sammy

@@@ javascript
// app.js
var app = $.sammy(function() { with(this) {

  get('#/user/:name', function() { with(this) {
    User.get(params['name'], function() {
      partial('user.html.erb', {user: user});
    });
  }});
  
  post('#/user/', function() { with(this) {
    User.create(params['user'], function(user) {
      redirect('#/user/' + user.name);
    });
  }});
  
}});
@@@

!SLIDE

# Why?

!SLIDE

# 1. Structure without the weight

_Like &lt;10K for real._

!SLIDE

# 2. Single Page Apps

_I know you be sweatin' gmail._

!SLIDE

# 3. Fully JavaScript applications with CouchDB/App

_Turtles all the way down (with a crunchy erlang center)_

!SLIDE

# 4. Because it was fun

_I like Javascript_

!SLIDE

# Really . . .

!SLIDE

## Sammy is RESTful evented Javascript.

!SLIDE

# DEMO 

_Please don't fuck this up . . ._

!SLIDE

# THANKS!

## http://code.quirkey.com/sammy

### Aaron Quint
### Quirkey NYC, LLC
### aaron@quirkey.com
### twitter.com/aq
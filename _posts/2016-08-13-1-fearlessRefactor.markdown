---
layout:     post
title:      "2"
subtitle:   "weekly learning"
date:       2016-08-13 00:00:00
author:     "ilake"
header-img: "img/post-bg-weekly.jpg"
tags:
    - weekly
---
> “strive 8/7 ~ now”

## Use
* <p>[Gem] <a href="https://github.com/solnic/virtus">virtus</a></p>

* <p>[Gem] <a href="https://github.com/NoamB/sorcery">sorcery</a></p>
  1. authentication for Rails

* <p>[Gem] <a href="https://github.com/thoughtbot/capybara-webkit">capybara-webkit</a></p>
  1. A Capybara driver for headless WebKit to test JavaScript web apps

* <p>[Gem] <a href="https://github.com/jnicklas/capybara">capybara</a></p>
  1. Acceptance test framework for web applications

* <p>[Gem] <a href="https://github.com/DatabaseCleaner/database_cleaner">database_cleaner</a></p>
  1. Strategies for cleaning databases

* <p>[Gem] <a href="https://github.com/jpignata/temping">temping</a></p>
  1. model mockup, dynamic create db table for model test

* <p>[Gem] <a href="https://github.com/whitesmith/rubycritic">rubycritic</a></p>
  1. provide a quality report of your Ruby code.

* <p>[Gem] <a href="https://github.com/kakas/CapistranoDeployTest">CapistranoDeployTest</a></p>
  1. Deploying a Rails App on Ubuntu 14.04 with Capistrano, Nginx, and Puma

## Read
* <p>[Ruby] <a href="http://api.rubyonrails.org/v4.1.4/classes/ActionController/Metal.html#method-i-performed-3F">ActionController::Metal#performed?</a></p>
  1. you can test whether render or redirect already happended

* <p>[Ruby] <a href="http://api.rubyonrails.org/classes/ActiveModel/Validations.html#method-i-valid-3F">ActiveModel::Validations#valid?(context=nil)</a></p>
  * validates_length_of :slug, minimum: 3, on: :user
  * validates_length_of :slug, minimum: 1, on: :admin
  * @user.save(context: :admin), @user.valid?(:admin), @user.valid?(:user),

* <p>[Ruby] <a href="http://railsfun.tw/t/ruby-queue-v-s-thread-mutex/619/2">[ruby 的多工]Queue v.s. Thread ? & Mutex …</a></p>

* <p>[Ruby] <a href="http://blog.codeclimate.com/blog/2012/10/17/7-ways-to-decompose-fat-activerecord-models/">7-ways-to-decompose-fat-activerecord-models</a></p>
    1. Value Objects: define domain-specific Value Objects,  Value Objects are great when you have an attribute or small group of attributes that have logic associated with them
    2. Service Objects: action is complex,  action reaches across multiple models, action interacts with an external service, action is not a core concern of the underlying model
    3. Form Objects: Virtus, When multiple ActiveRecord models might be updated by a single form submission, a Form Object can encapsulate the aggregation
    4. Query Objects: For complex SQL queries littering the definition of your ActiveRecord subclass
    5. View Objects: If logic is needed purely for display purposes, it does not belong in the model.
    6. Policy Objects: Sometimes complex read operations might deserve their own objects
      * “Service Object” for write operations and “Policy Object” for reads, Query Objects focus on executing SQL to return a result set
    7. Decorators: For cases where callback logic only needs to run in some circumstances or including it in the model would give the model too many responsibilities, a Decorator is useful

* <p>[CI] <a href="https://circleci.com/docs/parallel-manual-setup/">circle parallel-manual-setup</a></p>

* <p>[API] <a href="http://apionrails.icalialabs.com/book/chapter_five">api on rails, Authenticating users</a></p>

* <p>[Ruby] <a href="http://www.virtuouscode.com/2012/08/31/configuring-database_cleaner-with-rails-rspec-capybara-and-selenium/">Configuring database_cleaner with Rails, RSpec, Capybara, and Selenium</a></p>
  1. different cleaner strategy settings

* <p>[Ruby] routing constraints </p>
  1. <p>[Ruby] <a href="http://blog.arkency.com/2014/01/short-urls-for-every-route-in-your-rails-app/">Pretty, short urls for every route in your Rails app</a></p>
  2. <p>[Ruby] <a href="https://8thlight.com/blog/ben-voss/2013/01/12/how-to-use-rails-route-constraints.html">How to use rails routing constraints</a></p>
    * security vulnerabilities and data type validation
    * encapsulate and simplify actions (and supporting code)
  3. <p>[Ruby] <a href="https://www.viget.com/articles/using-routing-constraints-to-root-your-app">Using Routing Constraints to Root Your App</a></p>

* <p>[Ruby] <a href="https://ruby-china.org/topics/30233">use_transactional_fixtures vs database_cleaner</a></p>

## Book
* <p> <a href="http://openhome.cc/Gossip/CodeData/EssentialJavaScript/index.html">JavaScript 語言核心</a></p>
  * done (1), (2)

* <p> <a href="https://gumroad.com/l/ios-on-rails">ios on rails</a></p>

  * rails api design

* <p> <a href="http://rails-refactoring.com/">Fearless Rails Refactoring</a></p>

  * Refactoring recipes

     * Inline controller filters
         * extract filter to service

     * Explicitly render views with locals
         * pass the params to partials explicitly with render

     * Extract render/redirect methods
         * extract a private method for each render and redirect call

     * Extract a Single Action Controller class
         * extract like CreateProductsController only when ProductsController is too too too large

     * Extract routing constraint
         * use routing constraint to seperate controller action

     * Extract an adapter object
         * extract call external library to adapter object call

     * Extract a repository object
         * hide the direct ActiveRecord calls, isolated, add data storage on repo object

     * Extract a service object using the SimpleDelegator
         * move some domain or business logic to service object

     * Extract conditional validation into Service Object
         * when validation only used in one place, drop the condition on model, move it to service object

     * Extract a form object
         * move form to form object, more explicit and domain is expressed better
         * form object can't have save method (SRP), Persistence is a seperate concern and different object should take care of it, form object only valid data

  *  Patterns

     * Instantiating service objects
       *

     * The repository pattern
       *

     * Wrap external API with an adapter
         * isolated our interface from the implementation

     * 4 ways to early return from a rails controller

         * extracted_method; return if performed?

     * Service::Input
       *

     * Validations: Contexts
       *

     * Validations: Objectify
       *

  * Related topics

     * Service controller communication
         * True/false; return the object created/updated; return a response object that contains all the data and/or errors;
         * carry data through exceptions; controller passes callback methods;

     * Where to keep services
         * group your services according to the feature and then surround them with proper namespace
         * ex: Reporting::MonthlyReport, Forum::CreateNewTopic, TimeTracking::LogTimeService

     * Routing constraints
         * use routing constraints for situations where you need to choose differentctions based on some params
         * This makes the controller thinner and it’s more explicit what actios happening

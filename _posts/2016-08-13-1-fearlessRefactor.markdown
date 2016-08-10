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
  1.

* <p>[Gem] <a href="https://github.com/NoamB/sorcery">sorcery</a></p>
  1. authentication for Rails

## Read
* <p>[Ruby] <a href="http://api.rubyonrails.org/v4.1.4/classes/ActionController/Metal.html#method-i-performed-3F">ActionController::Metal#performed?</a></p>
  1. you can test whether render or redirect already happended

* <p>[Ruby] <a href="http://api.rubyonrails.org/classes/ActiveModel/Validations.html#method-i-valid-3F">ActiveModel::Validations#valid?(context=nil)</a></p>
  * validates_length_of :slug, minimum: 3, on: :user
  * validates_length_of :slug, minimum: 1, on: :admin
  * @user.save(context: :admin), @user.valid?(:admin), @user.valid?(:user),

* <p>[Ruby] <a href="http://railsfun.tw/t/ruby-queue-v-s-thread-mutex/619/2">[ruby 的多工]Queue v.s. Thread ? & Mutex …</a></p>

## Book
* <p> <a href="http://rails-refactoring.com/">Fearless Rails Refactoring</a></p>

  * #### Refactoring recipes

     * ##### Inline controller filters
         * extract filter to service

     * ##### Explicitly render views with locals
         * pass the params to partials explicitly with render

     * ##### Extract render/redirect methods
         * extract a private method for each render and redirect call

     * ##### Extract a Single Action Controller class
         * extract like CreateProductsController only when ProductsController is too too too large

     * ##### Extract routing constraint
         * use routing constraint to seperate controller action

     * ##### Extract an adapter object
         * extract call external library to adapter object call

     * ##### Extract a repository object
         * hide the direct ActiveRecord calls, isolated, add data storage on repo object

     * ##### Extract a service object using the SimpleDelegator
         * move some domain or business logic to service object

     * ##### Extract conditional validation into Service Object
         * when validation only used in one place, drop the condition on model, move it to service object

     * ##### Extract a form object
         * move form to form object, more explicit and domain is expressed better
         * form object can't have save method (SRP), Persistence is a seperate concern and different object should take care of it, form object only valid data

  * #### Patterns

     * ##### Instantiating service objects
       *

     * ##### The repository pattern
       *

     * ##### Wrap external API with an adapter
         * isolated our interface from the implementation

     * ##### 4 ways to early return from a rails controller

         * extracted_method; return if performed?

     * ##### Service::Input
       *

     * ##### Validations: Contexts
       *

     * ##### Validations: Objectify
       *

  * #### Related topics

     * ##### Service controller communication
         * True/false; return the object created/updated; return a response object that contains all the data and/or errors;
         * carry data through exceptions; controller passes callback methods;

     * ##### Where to keep services
         * group your services according to the feature and then surround them with proper namespace
         * ex: Reporting::MonthlyReport, Forum::CreateNewTopic, TimeTracking::LogTimeService

     * ##### Routing constraints
         * use routing constraints for situations where you need to choose differentctions based on some params
         * This makes the controller thinner and it’s more explicit what actios happening

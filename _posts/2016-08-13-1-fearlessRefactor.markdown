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
       * 123

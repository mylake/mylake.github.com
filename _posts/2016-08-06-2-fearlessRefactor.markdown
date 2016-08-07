---
layout:     post
title:      "2"
subtitle:   "weekly learning"
date:       2016-08-07 00:00:00
author:     "ilake"
header-img: "img/post-bg-weekly.jpg"
tags:
    - weekly
---
> “strive 8/7 ~ now”

## Book
* <p> <a href="http://rails-refactoring.com/">Fearless Rails Refactoring</a></p>

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
    * Extract call external library to adapter object call

  * ##### Extract a repository object
    * Hide the direct ActiveRecord calls, isolated, add data storage on repo object

  * ##### Extract a service object using the SimpleDelegator

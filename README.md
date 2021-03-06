# Bongloy's Terms of Service

[![Build Status](https://travis-ci.org/bongloy/bongloy-terms.svg?branch=master)](https://travis-ci.org/bongloy/bongloy-terms)

Bongloy's terms of service. Browse here for previous versions and diffs.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'bongloy-terms'
```

## Usage

To include Bongloy's terms into a Rails application add the following helper method to your `ApplicationController`

```ruby
class ApplicationController < ActionController::Base
  helper_method :bongloy_terms_renderer

  def bongloy_terms_renderer
    @bongloy_terms_renderer ||= Bongloy::Terms::Renderer.new
  end
end
```

Then you can use it in your views like

```erb
  <%= bongloy_terms_renderer.render('terms').html_safe %>
  <%= bongloy_terms_renderer.render('privacy').html_safe %>
  <%= bongloy_terms_renderer.render('prohibited_businesses').html_safe %>
  <%= bongloy_terms_renderer.render('high_risk_mcc_categories').html_safe %>
```

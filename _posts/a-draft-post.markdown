---
title: Setting up a Rails App
description: Work in progress
published: true
---
## Adding custom error messages to validation errors in Rails 5

**For an overall guide to Rails Validation, see [http://guides.rubyonrails.org/active_record_validations.html](http://guides.rubyonrails.org/active_record_validations.html)**

From that guide:

```ruby
class Person < ApplicationRecord
  # Hard-coded message
  validates :name, presence: { message: "must be given please" }
 
  # Message with dynamic attribute value. %{value} will be replaced with
  # the actual value of the attribute. %{attribute} and %{model} also
  # available.
  validates :age, numericality: { message: "%{value} seems wrong" }
 
  # Proc
  validates :username,
    uniqueness: {
      # object = person object being validated
      # data = { model: "Person", attribute: "Username", value: <username> }
      message: ->(object, data) do
        "Hey #{object.name}!, #{data[:value]} is taken already! Try again #{Time.zone.tomorrow}"
      end
    }
end
```

But this does not explain how to change the actual attribute name as displayed in the message. Instead of "Email cannot be blank", I might want "Please enter your email address", with lower case used. How to deal with this?
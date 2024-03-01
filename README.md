<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-learn/terraspace-restricting-envs/blob/master/README.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

# Terraspace Restricting Environments

[![BoltOps Learn Badge](https://img.boltops.com/boltops-learn/boltops-learn.png)](https://learn.boltops.com)

[![BoltOps Badge](https://img.boltops.com/boltops/badges/boltops-badge.png)](https://www.boltops.com)

An example Terraspace project to show how to restrict the environments that can be deployed:

config/app.rb

```ruby
Terraspace.configure do |config|
  config.allow.envs = ["dev", "prod"]
  # config.deny.envs = ["qa"]
end
```

## Usage

Uncomment the examples in `config/app.rb` and run:

    TS_ENV=dev  terraspace up stack1
    TS_ENV=prod terraspace up stack1
    TS_ENV=qa   terraspace up stack1

## Video

[![Watch the video](https://uploads-learn.boltops.com/0pmf9suoztwfqub327wtk49gdygx)](https://learn.boltops.com/courses/terraspace-fundamentals/lessons/terraspace-restricting-environments)

Note: Premium video content requires a subscription.
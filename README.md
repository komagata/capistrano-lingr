# Capistrano::Lingr

Notify to Lingr after deploy by Capistrano

## Installation

Add this line to your application's Gemfile:

```rb
gem 'capistrano-lingr'
```

And then execute: `bundle install`

## Usage

In `config/deploy.rb`

```rb
require 'capistrano/lingr'
		
set :lingr_config, {
  :room_id => "hoge",
  :bot_id  => "huga",
  :secret  => "piyo"
}

after :deploy, 'notify:lingr'
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

source 'https://rubygems.org'

group :rake do
  puppetversion = ENV.key?('PUPPET_VERSION') ? "#{ENV['PUPPET_VERSION']}" : ['>= 3.0.0','< 5.0']
  gem 'puppet', puppetversion
  gem 'puppet-lint'
  gem 'puppetlabs_spec_helper', '>=0.2.0'
  # removed method last_comment (requires rspec 3.5.0)
  gem 'rake'
  gem 'rspec-system-puppet',     :require => false
  gem 'highline'
  if RUBY_VERSION <= "1.9.0"
    gem 'json', '< 2.0' # newer versions requires at least ruby 2.0
    gem 'json_pure', '< 2.0.0'
    gem 'fog-google', '< 0.1.1'
    gem 'rspec-core'
  else
    gem 'rspec-core', '>= 3.5.0'
  end
  gem 'rspec-puppet'
  gem 'metadata-json-lint',      :require => false
  if RUBY_VERSION >= "2.2.0"
    gem 'safe_yaml'
  end
  gem 'xmlrpc'
  if RUBY_VERSION < "2.1.0"
    gem 'nokogiri', '< 1.7.0'
  end
end

group :development do
  gem 'puppet-blacksmith',  '>= 3.0'
  gem 'librarian-puppet' , '>=2.0'
end

# encoding: utf-8

require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "vebdew"
  gem.homepage = "http://github.com/eggegg/vebdew"
  gem.license = "MIT"
  gem.summary = %Q{HTML5 slides generator}
  gem.description = %Q{Generate HTML5 slides}
  gem.email = "andrewliu33@gmail.com"
  gem.authors = ["Andrew Liu"]
  # dependencies defined in Gemfile
end
Jeweler::RubygemsDotOrgTasks.new

desc 'Run test'
task :test do
  sh "bundle exec bacon -a"
end

task :default => :test

require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "vebdew #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

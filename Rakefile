# # Add your own tasks in files placed in lib/tasks ending in .rake,
# # for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

# require File.expand_path('../config/application', __FILE__)

# module TempFixForRakeLastComment
#   def last_comment
#     last_description
#   end 
# end

# Rails.application.load_tasks
  require File.expand_path('../config/application', __FILE__)
  require 'rake'
  #require 'resque/tasks'

# temp fix for NoMethodError: undefined method `last_comment'
 # remove when fixed in Rake 11.x
 module TempFixForRakeLastComment
   def last_comment
     last_description
   end 
 end
 Rake::Application.send :include, TempFixForRakeLastComment
 ### end of temfix
 
  task "resque:preload" => :environment

  Rails.application.load_tasks
namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola desde Rake!"
  end 
end 

namespace :db do
  desc 'migrate changes to your database'
  task migrate: :environment do #run environment task before it can migrate
    Student.create_table 
  end 
end 

task :environment do
  require_relative './config/environment'
end 

namespace :db do
  desc 'seed the database with some dummy data'
  task seed: :environment do #run environment task before it can seed
    require_relative './db/seeds'
  end 
end 

desc 'drop into the Pry console'
task console: :environment do
  Pry.start 
end 

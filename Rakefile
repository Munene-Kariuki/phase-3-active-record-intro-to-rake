namespace :greeting do 
  desc "outputs hello to the terminal"
  task :hello do
    puts "hello from Rake!"
  end

  desc "outputs holla to the terminal"
  task :hola do 
    puts "hola de Rake!"
  end  
end  

namespace :db do
  desc "migrate changes to your database"
  task migrate: :enviroment do
    Student.create_table
  end

  desc "seed database with some dummy data"
  task seed: :enviroment do 
    require_relative './db/seeds'
  end  
end

task :enviroment do
  require_relative './config/environment'
end

desc "drop into the pry console"
task console: :enviroment do 
  Pry.start
end  

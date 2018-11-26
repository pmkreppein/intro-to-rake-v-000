require 'pry'

task :environment do
  require_relative './config/environment'
end

desc 'hello'
namespace :greeting do
  task :hello do
    puts 'hello from Rake!'
  end

  desc 'hola'
  task :hola do
    puts 'hola de Rake!'
  end
end

namespace :db do
  desc 'migrate'
  task migrate: :environment do
    Student.create_table
  end

  desc 'seed'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

desc 'pry'
task console: :environment do
  Pry.start
end
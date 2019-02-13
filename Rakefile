def run_command(command)
  system(command)
end

def run_in_parallel
  command = 'bundle exec parallel_cucumber --first-is-1 -n 4  --group-by scenarios -- features'

  system(command)
end

task 'task_2' do
  puts 'Doing Task 2!'

  run_in_parallel
end

task 'task_1' do
  command = 'bundle exec rake task_2'
  run_command(command)

  puts 'Task 1 done!'
end

task :default do
  Rake::Task['task_1'].invoke

  puts 'All done!'
end
